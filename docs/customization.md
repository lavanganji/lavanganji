# Customization Guide

## 🎨 Themes and Colors

### Available Themes
- `default` - Classic GitHub colors
- `dark` - Dark mode theme
- `radical` - Pink and purple gradient
- `merko` - Green theme
- `gruvbox` - Vintage theme
- `tokyonight` - Purple dark theme
- `onedark` - Atom One Dark theme
- `cobalt` - Blue theme
- `synthwave` - Neon theme
- `highcontrast` - High contrast theme
- `dracula` - Dracula theme

### Custom Color Codes
You can customize colors using hex codes:

```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=lavanganji&bg_color=1a1b27&text_color=9f9f9f&icon_color=bd93f9&title_color=bd93f9)
```

## 🛠️ Badge Customization

### Technology Badges
```markdown
![Badge](https://img.shields.io/badge/-Technology-COLOR?style=STYLE&logo=LOGO&logoColor=white)
```

**Styles:**
- `flat` - Flat design
- `flat-square` - Flat with square edges
- `for-the-badge` - Large badge
- `plastic` - Plastic appearance
- `social` - Social media style

**Popular Technology Colors:**
- JavaScript: `F7DF1E`
- Python: `3776AB`
- React: `61DAFB`
- Node.js: `339933`
- HTML5: `E34F26`
- CSS3: `1572B6`
- Docker: `2496ED`
- Kubernetes: `326CE5`

### Social Media Badges
```markdown
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](URL)
[![Twitter](https://img.shields.io/badge/-Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](URL)
[![Instagram](https://img.shields.io/badge/-Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](URL)
```

## 📊 Stats Customization

### GitHub Stats Parameters
```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=USERNAME&PARAMETERS)
```

**Available Parameters:**
- `show_icons=true` - Show icons
- `count_private=true` - Count private repos
- `theme=THEME` - Color theme
- `hide=stars,commits,prs,issues,contribs` - Hide specific stats
- `include_all_commits=true` - Include all commits
- `line_height=27` - Line height
- `title_color=COLOR` - Title color
- `text_color=COLOR` - Text color
- `icon_color=COLOR` - Icon color
- `bg_color=COLOR` - Background color
- `border_color=COLOR` - Border color

### Language Stats Parameters
```markdown
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=USERNAME&PARAMETERS)
```

**Available Parameters:**
- `layout=compact` - Compact layout
- `theme=THEME` - Color theme
- `hide=html,css` - Hide specific languages
- `langs_count=8` - Number of languages to show
- `exclude_repo=repo1,repo2` - Exclude repositories
- `card_width=445` - Card width

### Streak Stats Parameters
```markdown
![Streak](https://github-readme-streak-stats.herokuapp.com/?user=USERNAME&PARAMETERS)
```

**Available Parameters:**
- `theme=THEME` - Color theme
- `hide_border=true` - Hide border
- `background=COLOR` - Background color
- `border=COLOR` - Border color
- `stroke=COLOR` - Stroke color
- `ring=COLOR` - Ring color
- `fire=COLOR` - Fire color
- `currStreakNum=COLOR` - Current streak number color
- `sideNums=COLOR` - Side numbers color
- `currStreakLabel=COLOR` - Current streak label color
- `sideLabels=COLOR` - Side labels color
- `dates=COLOR` - Dates color

## 🎭 Typing Animation Customization

```markdown
![Typing SVG](https://readme-typing-svg.herokuapp.com?font=FONT&pause=PAUSE&color=COLOR&width=WIDTH&lines=LINE1;LINE2;LINE3)
```

**Parameters:**
- `font=Fira+Code` - Font family
- `size=22` - Font size
- `pause=1000` - Pause between lines (ms)
- `color=F75C7E` - Text color
- `background=FFFFFF00` - Background color (transparent)
- `center=true` - Center align
- `vCenter=true` - Vertical center
- `width=435` - Animation width
- `height=50` - Animation height
- `lines=Text+Line+1;Text+Line+2` - Text lines (URL encoded)
- `duration=5000` - Animation duration

**Popular Fonts:**
- `Fira+Code`
- `JetBrains+Mono`
- `Roboto+Mono`
- `Source+Code+Pro`
- `Ubuntu+Mono`

## 🏆 Trophy Customization

```markdown
![Trophy](https://github-profile-trophy.vercel.app/?username=USERNAME&PARAMETERS)
```

**Parameters:**
- `theme=THEME` - Color theme
- `column=7` - Number of columns
- `row=1` - Number of rows
- `margin-w=15` - Margin width
- `margin-h=15` - Margin height
- `no-bg=false` - No background
- `no-frame=false` - No frame
- `rank=SECRET,SSS,SS,S,AAA,AA,A,B,C` - Show specific ranks

**Available Themes:**
- `flat`, `onedark`, `gruvbox`, `dracula`, `monokai`, `chalk`, `nord`, `alduin`, `darkhub`, `juicyfresh`, `buddhism`, `oldie`, `radical`, `onestar`, `discord`, `algolia`, `gitdimmed`, `tokyonight`, `matrix`, `apprentice`, `dark_dimmed`

## 🎨 Profile Views Customization

### Komarev Counter
```markdown
![Profile Views](https://komarev.com/ghpvc/?username=USERNAME&color=COLOR&style=STYLE&label=LABEL)
```

**Styles:**
- `flat` - Flat design
- `flat-square` - Flat with square corners
- `for-the-badge` - Large badge style
- `plastic` - Plastic appearance

**Colors:**
- `blue`, `green`, `red`, `orange`, `yellow`, `purple`, `pink`, `grey`, `brightgreen`, `lightgrey`

### Visitor Badge
```markdown
![Visitors](https://visitor-badge.laobi.icu/badge?page_id=USERNAME.REPOSITORY&title=TITLE&left_color=COLOR&right_color=COLOR)
```

## 🐍 Snake Animation Customization

The snake animation can be customized by modifying the workflow file:

```yaml
- uses: Platane/snk/svg-only@v3
  with:
    github_user_name: USERNAME
    outputs: |
      dist/github-contribution-grid-snake.svg
      dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      dist/github-contribution-grid-snake-light.svg?palette=github-light
```

**Available Palettes:**
- `github` - Default GitHub colors
- `github-dark` - GitHub dark mode
- `github-light` - GitHub light mode
- Custom palettes can be defined

## 📱 Responsive Design

### Mobile-Friendly Layouts
```markdown
<div align="center">
  <img src="URL" alt="Description" style="max-width: 100%;" />
</div>
```

### Flexible Widths
```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=USERNAME&card_width=400)
```

## 🎵 Additional Widgets

### Spotify Now Playing
```markdown
![Spotify](https://spotify-github-profile.vercel.app/api/spotify-playing)
```

### Quote of the Day
```markdown
![Quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=THEME)
```

### WakaTime Stats
Add to your README between the comments:
```markdown
<!--START_SECTION:waka-->
<!--END_SECTION:waka-->
```

## 🔧 Advanced Customizations

### Custom Metrics
You can create custom metrics using GitHub Actions and external APIs.

### Dynamic Content
Use GitHub Actions to update content automatically:
- Latest blog posts
- Recent GitHub activity
- Current time in different timezones
- Random quotes or facts

### Interactive Elements
- Collapsible sections using HTML details/summary
- Hover effects with CSS
- Click tracking with UTM parameters
