# Profile Configuration

This file contains customizable settings for your GitHub profile. Edit these values to personalize your profile.

## Personal Information
```yaml
profile:
  name: "Your Name"
  username: "lavanganji"
  title: "Full Stack Developer"
  location: "Your Location"
  email: "your.email@example.com"
  website: "https://yourwebsite.com"
  
taglines:
  - "Full Stack Developer"
  - "Open Source Enthusiast" 
  - "Always Learning New Things"
  - "Problem Solver"
  - "Code Craftsman"

bio:
  current_work: "Your Current Project"
  learning: "Technologies you're learning"
  collaboration: "Open Source Projects"
  help_with: "What you need help with"
  expertise: "Your expertise areas"
  pronouns: "Your pronouns"
  fun_fact: "A fun fact about you"

contact:
  linkedin: "https://linkedin.com/in/yourprofile"
  twitter: "https://twitter.com/yourhandle"
  email: "your.email@example.com"
  portfolio: "https://yourportfolio.com"
  discord: "https://discord.gg/yourinvite"

support:
  buymeacoffee: "https://buymeacoffee.com/yourprofile"
  kofi: "https://ko-fi.com/yourprofile"
  patreon: "https://patreon.com/yourprofile"
```

## Theme Settings
```yaml
theme:
  primary: "tokyonight"
  stats: "tokyonight"
  streak: "tokyonight"
  trophies: "tokyonight"
  activity: "tokyo-night"
  
colors:
  primary: "#bd93f9"
  secondary: "#50fa7b"
  accent: "#f1fa8c"
  background: "#282a36"
  text: "#f8f8f2"
```

## Technologies
```yaml
languages:
  - name: "Python"
    color: "3776AB"
    logo: "Python"
  - name: "JavaScript"
    color: "F7DF1E"
    logo: "JavaScript"
  - name: "TypeScript"
    color: "3178C6"
    logo: "TypeScript"
  - name: "Java"
    color: "007396"
    logo: "Java"
  - name: "C++"
    color: "00599C"
    logo: "C%2B%2B"

frontend:
  - name: "React"
    color: "61DAFB"
    logo: "React"
  - name: "Vue.js"
    color: "4FC08D"
    logo: "Vue.js"
  - name: "HTML5"
    color: "E34F26"
    logo: "HTML5"
  - name: "CSS3"
    color: "1572B6"
    logo: "CSS3"
  - name: "Sass"
    color: "CC6699"
    logo: "Sass"

backend:
  - name: "Node.js"
    color: "339933"
    logo: "Node.js"
  - name: "Express.js"
    color: "000000"
    logo: "Express"
  - name: "Django"
    color: "092E20"
    logo: "Django"
  - name: "Flask"
    color: "000000"
    logo: "Flask"

databases:
  - name: "MongoDB"
    color: "47A248"
    logo: "MongoDB"
  - name: "PostgreSQL"
    color: "336791"
    logo: "PostgreSQL"
  - name: "MySQL"
    color: "4479A1"
    logo: "MySQL"
  - name: "Redis"
    color: "DC382D"
    logo: "Redis"

devops:
  - name: "Docker"
    color: "2496ED"
    logo: "Docker"
  - name: "Kubernetes"
    color: "326CE5"
    logo: "Kubernetes"
  - name: "AWS"
    color: "232F3E"
    logo: "Amazon-AWS"
  - name: "Git"
    color: "F05032"
    logo: "Git"
  - name: "VS Code"
    color: "007ACC"
    logo: "Visual-Studio-Code"
```

## Featured Projects
```yaml
projects:
  - name: "Project Name 1"
    description: "Brief description of your amazing project"
    url: "https://github.com/lavanganji/project1"
    tech_stack: ["React", "Node.js", "MongoDB", "Express"]
    
  - name: "Project Name 2"
    description: "Another cool project description"
    url: "https://github.com/lavanganji/project2"
    tech_stack: ["Python", "Django", "PostgreSQL", "Docker"]
    
  - name: "Project Name 3"
    description: "Describe your third project"
    url: "https://github.com/lavanganji/project3"
    tech_stack: ["Vue.js", "Firebase", "TypeScript", "Tailwind CSS"]
```

## Workflow Settings
```yaml
workflows:
  wakatime:
    enabled: true
    schedule: "30 18 * * *"  # 12am IST
    
  blog_posts:
    enabled: true
    schedule: "0 * * * *"    # Every hour
    feeds:
      - "https://dev.to/feed/lavanganji"
      
  snake:
    enabled: true
    schedule: "0 */24 * * *"  # Every 24 hours
    
  stats_update:
    enabled: true
    schedule: "0 */12 * * *"  # Every 12 hours
    
  profile_views:
    enabled: true
    schedule: "0 */6 * * *"   # Every 6 hours
```

## Display Settings
```yaml
display:
  show_visitor_count: true
  show_github_stats: true
  show_streak_stats: true
  show_language_stats: true
  show_trophies: true
  show_activity_graph: true
  show_snake_animation: true
  show_blog_posts: true
  show_projects: true
  show_skills_badges: true
  show_social_links: true
  show_support_links: true
  
stats:
  count_private_repos: true
  show_icons: true
  include_all_commits: true
  languages_count: 8
  
animation:
  typing_speed: 50
  pause_duration: 1000
  font: "Fira Code"
```

## Content Settings
```yaml
content:
  max_blog_posts: 5
  max_projects: 3
  show_last_updated: true
  
sections:
  about_me: true
  technologies: true
  github_stats: true
  trophies: true
  projects: true
  blog_posts: true
  contact: true
  support: false
```
