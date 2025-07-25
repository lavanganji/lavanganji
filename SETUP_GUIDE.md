# GitHub Profile Setup Guide 🚀

This guide will help you set up an amazing GitHub profile with automated features and visitor counters.

## 📁 Repository Structure

Your GitHub profile repository should have this structure:

```
lavanganji/
├── README.md                 # Your profile README (this displays on your profile)
├── .github/
│   └── workflows/
│       ├── blog-post-workflow.yml    # Auto-update blog posts
│       ├── waka-readme.yml          # Wakatime stats
│       └── snake.yml                # Contribution snake animation
├── assets/
│   ├── images/              # Profile images, banners
│   └── gifs/               # Animated GIFs
└── docs/
    └── setup-guide.md      # This file
```

## 🔧 Automated Features Setup

### 1. Wakatime Stats (Coding Activity)

Create `.github/workflows/waka-readme.yml`:

```yaml
name: Waka Readme

on:
  schedule:
    # Runs at 12am IST
    - cron: '30 18 * * *'
  workflow_dispatch:

jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: ubuntu-latest
    steps:
      - uses: anmol098/waka-readme-stats@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
          SHOW_OS: "True"
          SHOW_PROJECTS: "True"
          SHOW_PROFILE_VIEWS: "False"
          SHOW_EDITORS: "True"
          SHOW_LANGUAGE_PER_REPO: "True"
          SHOW_LOC_CHART: "False"
          SHOW_LINES_OF_CODE: "True"
          SHOW_SHORT_INFO: "True"
```

**Setup Steps:**
1. Sign up at [Wakatime](https://wakatime.com/)
2. Get your API key from Wakatime dashboard
3. Add `WAKATIME_API_KEY` to your repository secrets
4. Add `GH_TOKEN` with repo permissions to secrets

### 2. Blog Post Workflow

Create `.github/workflows/blog-post-workflow.yml`:

```yaml
name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *' # Runs every hour
  workflow_dispatch: # Run workflow manually (without waiting for the cron to be called)

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Pull in dev.to posts
        uses: gautamkrishnar/blog-post-workflow@master
        with:
          comment_tag_name: "BLOG-POST-LIST"
          feed_list: "https://dev.to/feed/yourusername,https://yourblog.com/rss"
```

### 3. Snake Contribution Animation

Create `.github/workflows/snake.yml`:

```yaml
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: lavanganji
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## 🎨 Customization Tips

### Color Themes
- `tokyonight` - Dark theme with purple accents
- `dark` - Simple dark theme
- `radical` - Pink and purple theme
- `merko` - Green theme
- `gruvbox` - Retro theme
- `chartreuse-dark` - Green dark theme

### Badge Customization
Replace technology badges with your actual skills:

```markdown
![Your-Tech](https://img.shields.io/badge/-Your--Tech-COLOR?style=flat-square&logo=LOGO&logoColor=white)
```

Find more badges at [shields.io](https://shields.io/) and logos at [simple-icons](https://simpleicons.org/).

### Stats Customization

You can customize GitHub stats with various parameters:

```markdown
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=lavanganji&show_icons=true&theme=tokyonight&count_private=true&hide=issues&include_all_commits=true)
```

Parameters:
- `theme` - Color theme
- `count_private` - Include private repos
- `hide` - Hide specific stats (stars,commits,prs,issues,contribs)
- `show_icons` - Show icons
- `include_all_commits` - Include all commits

## 🔐 Repository Secrets Setup

Go to your repository Settings > Secrets and variables > Actions, then add:

1. **WAKATIME_API_KEY** - From wakatime.com dashboard
2. **GH_TOKEN** - Personal access token with repo permissions
3. **GITHUB_TOKEN** - Usually automatically available

## 📝 Content Ideas

### About Me Section
- Current role/position
- Technologies you're passionate about
- Current learning goals
- Fun facts or hobbies
- Professional achievements

### Projects Section
- Showcase 3-5 best projects
- Include live demos and source code links
- Explain the problem solved and technologies used
- Add screenshots or GIFs

### Skills Section
- Organize by categories (Frontend, Backend, DevOps, etc.)
- Use skill level indicators if desired
- Include both technical and soft skills
- Keep it updated with new learnings

## 🌟 Additional Features

### Spotify Now Playing
```markdown
![Spotify](https://novatorem-kyzbk7wxl-natemoo-re.vercel.app/api/spotify)
```

### Random Quotes
```markdown
![Quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight)
```

### Profile Trophy
```markdown
![Trophy](https://github-profile-trophy.vercel.app/?username=lavanganji&theme=tokyonight&no-frame=false&no-bg=false&margin-w=4)
```

### Typing Animation
```markdown
![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=F75C7E&width=435&lines=Your+Text+Here;Another+Line+Here)
```

## 🚀 Deployment

1. Copy the template content to your `README.md`
2. Replace placeholder text with your information
3. Set up the workflows if you want automated features
4. Commit and push to see your profile update!

## 🔄 Regular Maintenance

- Update your projects section quarterly
- Refresh your skills as you learn new technologies
- Keep your contact information current
- Review and update your bio annually

---

**Pro Tip:** Pin your profile repository for easy access and to show visitors you care about your GitHub presence!
