# Troubleshooting Guide

## 🔧 Common Issues and Solutions

### Workflow Issues

#### Wakatime Stats Not Updating
**Problem:** Wakatime stats section shows no data or outdated information.

**Solutions:**
1. **Check API Key:**
   ```bash
   # Verify your Wakatime API key is correct
   # Go to: https://wakatime.com/api-key
   # Add it to repository secrets as WAKATIME_API_KEY
   ```

2. **Check Permissions:**
   - Ensure GH_TOKEN has `repo` permissions
   - Token should have access to the repository

3. **Check Wakatime Integration:**
   - Install Wakatime plugin in your IDE
   - Ensure you're coding with the plugin active
   - Wait 24-48 hours for initial data

4. **Workflow Syntax:**
   ```yaml
   # Ensure proper indentation and syntax
   - uses: anmol098/waka-readme-stats@master
     with:
       WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
       GH_TOKEN: ${{ secrets.GH_TOKEN }}
   ```

#### Snake Animation Not Generating
**Problem:** Snake contribution animation doesn't appear.

**Solutions:**
1. **Check Username:**
   ```yaml
   # Make sure username is correct
   github_user_name: lavanganji  # Replace with actual username
   ```

2. **Check Permissions:**
   ```yaml
   jobs:
     generate:
       permissions: 
         contents: write  # Required permission
   ```

3. **Check Branch:**
   - Animation outputs to `output` branch
   - Reference it in README: `https://raw.githubusercontent.com/USERNAME/USERNAME/output/github-contribution-grid-snake.svg`

4. **Manual Trigger:**
   - Go to Actions tab
   - Select "Generate Snake Animation"
   - Click "Run workflow"

#### Blog Posts Not Updating
**Problem:** Blog post section remains empty or outdated.

**Solutions:**
1. **Check Feed URL:**
   ```yaml
   # Ensure feed URL is accessible
   feed_list: "https://dev.to/feed/lavanganji"  # Test this URL in browser
   ```

2. **Check Comment Tags:**
   ```markdown
   <!-- BLOG-POST-LIST:START -->
   <!-- BLOG-POST-LIST:END -->
   ```

3. **RSS Feed Requirements:**
   - Feed must be valid RSS/Atom format
   - Feed should be publicly accessible
   - Feed should contain recent posts

### Stats Display Issues

#### GitHub Stats Not Loading
**Problem:** GitHub stats images show error or don't load.

**Solutions:**
1. **Check Username:**
   ```markdown
   # Ensure username is correct (case-sensitive)
   ![Stats](https://github-readme-stats.vercel.app/api?username=lavanganji)
   ```

2. **Cache Issues:**
   ```markdown
   # Add cache busting parameter
   ![Stats](https://github-readme-stats.vercel.app/api?username=lavanganji&v=2)
   ```

3. **Vercel Deployment:**
   - Sometimes Vercel apps go down
   - Try alternative: `https://github-readme-stats-sigma-five.vercel.app/`

4. **Rate Limiting:**
   - Too many requests can cause temporary blocks
   - Wait a few minutes and try again

#### Profile Views Badge Not Working
**Problem:** Visitor counter shows wrong count or doesn't load.

**Solutions:**
1. **Check Service Status:**
   ```markdown
   # Try different visitor counter services
   ![Views](https://komarev.com/ghpvc/?username=lavanganji)
   ![Visitors](https://visitor-badge.laobi.icu/badge?page_id=lavanganji.lavanganji)
   ```

2. **Clear Cache:**
   - Hard refresh your browser (Ctrl+F5 / Cmd+Shift+R)
   - Try incognito/private mode

3. **Service Alternatives:**
   ```markdown
   # Multiple options available
   ![Count](https://count.getloli.com/get/@lavanganji)
   ![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Flavanganji)
   ```

### Repository Setup Issues

#### Secrets Not Working
**Problem:** Workflow fails due to missing or invalid secrets.

**Solutions:**
1. **Add Required Secrets:**
   - Go to Repository Settings → Secrets and variables → Actions
   - Add: `WAKATIME_API_KEY`, `GH_TOKEN`

2. **Token Permissions:**
   - Personal Access Token needs `repo` scope
   - For organizations, check SSO requirements

3. **Secret Names:**
   - Names are case-sensitive
   - Must match exactly in workflow files

#### Workflow Permissions
**Problem:** Workflows fail with permission errors.

**Solutions:**
1. **Repository Settings:**
   - Go to Settings → Actions → General
   - Set "Workflow permissions" to "Read and write permissions"

2. **GITHUB_TOKEN Permissions:**
   ```yaml
   permissions:
     contents: write
     actions: read
   ```

### Display and Formatting Issues

#### Images Not Showing
**Problem:** Badges or stats images don't display in README.

**Solutions:**
1. **Check URL Syntax:**
   ```markdown
   # Correct syntax
   ![Alt Text](https://example.com/image.svg)
   
   # Not this
   [Alt Text](https://example.com/image.svg)
   ```

2. **URL Encoding:**
   ```markdown
   # Special characters need encoding
   ![Badge](https://img.shields.io/badge/-C%2B%2B-blue)  # C++ encoded
   ```

3. **GitHub Caching:**
   - GitHub caches images
   - Add `?v=1` parameter to force refresh

#### Markdown Formatting Issues
**Problem:** README formatting appears broken.

**Solutions:**
1. **Check Markdown Syntax:**
   ```markdown
   # Headers need space after #
   ## Correct Header
   
   #Incorrect Header
   ```

2. **HTML in Markdown:**
   ```html
   <!-- Ensure proper closing tags -->
   <div align="center">
     <img src="url" alt="alt" />
   </div>
   ```

3. **Line Breaks:**
   ```markdown
   <!-- Use two spaces for line breaks -->
   Line 1  
   Line 2
   
   <!-- Or use HTML -->
   Line 1<br>
   Line 2
   ```

### Performance Issues

#### Slow Loading Profile
**Problem:** Profile takes long time to load.

**Solutions:**
1. **Optimize Images:**
   - Use compressed images
   - Limit GIF file sizes (<10MB)
   - Use appropriate image formats

2. **Reduce API Calls:**
   - Limit number of external widgets
   - Use caching parameters

3. **Content Organization:**
   - Use collapsible sections for large content
   - Prioritize above-the-fold content

### GitHub Pages Issues

#### Snake Animation 404 Error
**Problem:** Snake animation shows 404 error.

**Solutions:**
1. **Check Output Branch:**
   ```bash
   # Verify output branch exists
   git branch -r | grep output
   ```

2. **Workflow Completion:**
   - Check if workflow completed successfully
   - Look for any error messages in Actions tab

3. **Correct URL:**
   ```markdown
   # Ensure correct repository and username
   ![Snake](https://raw.githubusercontent.com/lavanganji/lavanganji/output/github-contribution-grid-snake.svg)
   ```

## 🔍 Debugging Steps

### 1. Check Workflow Logs
- Go to Actions tab in repository
- Click on failed workflow
- Expand steps to see error messages

### 2. Validate External URLs
- Test all external URLs in browser
- Check for API rate limits
- Verify service status

### 3. Test Locally
```bash
# Clone your repository
git clone https://github.com/lavanganji/lavanganji.git

# Check for syntax errors
markdown-lint README.md
```

### 4. Use GitHub's Preview
- Edit README.md in GitHub web interface
- Use "Preview" tab to check rendering
- Look for broken images or formatting

## 📞 Getting Help

### Community Resources
- [GitHub Community Discussions](https://github.com/community)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/github)
- [Reddit r/github](https://reddit.com/r/github)

### Official Documentation
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://guides.github.com/features/mastering-markdown/)

### Service-Specific Help
- **Wakatime:** [Support](https://wakatime.com/help)
- **Vercel:** [GitHub Issues](https://github.com/anuraghazra/github-readme-stats/issues)
- **Shields.io:** [Documentation](https://shields.io/)

## 🚨 Emergency Fixes

### Quick Disable Workflows
```yaml
# Add to any workflow to disable it
if: false
```

### Minimal README Backup
```markdown
# Your Name

👋 Hi there! My profile is currently under maintenance.

![Profile Views](https://komarev.com/ghpvc/?username=lavanganji)

## 📫 Contact
- Email: your.email@example.com
- LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)
```

### Reset Repository
```bash
# If everything breaks, reset to minimal setup
git checkout main
git reset --hard HEAD~5  # Go back 5 commits
git push --force
```

Remember: Always test changes in a separate branch first!
