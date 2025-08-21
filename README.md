# Quarto RevealJS Presentation Template

A template repository for creating beautiful, minimalist presentations using Quarto RevealJS with the clean theme. This template includes automatic rendering and deployment to GitHub Pages using GitHub Actions.

[![Deploy Presentation](https://github.com/JacobKMcPherson/template_quarto_presentation/actions/workflows/render-and-deploy.yml/badge.svg)](https://github.com/JacobKMcPherson/template_quarto_presentation/actions/workflows/render-and-deploy.yml)

## ✨ Features

- 🎨 **Clean Theme**: Minimalist and elegant presentation design inspired by Kyle's LaTeX template
- 🚀 **Automatic Deployment**: GitHub Actions automatically renders and deploys your presentation
- 📱 **Responsive**: Works perfectly on any device or display size
- 🔧 **Easy Setup**: Just edit the `.qmd` file and push - everything else is handled automatically
- 🌐 **GitHub Pages**: Your presentation is automatically published online

### 🎪 Interactive Features

- **🖍️ Chalkboard Drawing** - Press `c` to draw on slides
- **📝 Notes Canvas** - Press `b` for note-taking overlay  
- **🗣️ Speaker View** - Press `s` for presenter notes and timer
- **📜 Scroll View** - Press `r` to scroll through slides
- **🔍 Overview Mode** - Press `o` to see all slides at once
- **⬛ Fullscreen** - Press `f` for distraction-free presenting
- **📚 Slide Menu** - Hamburger menu for navigation
- **🔗 GitHub Footer** - Direct link back to repository
- **📡 Multiplex Ready** - Easy setup for synchronized presentations

## 🚀 Quick Start

1. **Use this template**: Click the "Use this template" button on GitHub
2. **Clone your repository**: `git clone https://github.com/yourusername/your-repo-name.git`
3. **Edit the presentation**: Modify `template.qmd` with your content
4. **Enable GitHub Pages**: 
   - Go to Settings → Pages
   - Set Source to "GitHub Actions"
5. **Push changes**: Your presentation will automatically build and deploy!

Your presentation will be available at: `https://yourusername.github.io/your-repo-name/`

## 🎯 Live Example

You can see this template in action at: [https://jacobkmcpherson.github.io/template_quarto_presentation/](https://jacobkmcpherson.github.io/template_quarto_presentation/) (after the workflow runs)

## 📝 Customization

### Edit Your Presentation

The main presentation file is `template.qmd`. Update the YAML frontmatter with your details:

```yaml
---
title: "Your Presentation Title"
subtitle: "Your subtitle"
author:
  - name: Your Name
    email: your.email@domain.com
    affiliations: Your Institution
date: last-modified
---
```

### Theme Customization

The clean theme provides several special classes for enhanced formatting:

- `.alert` class for emphasis: [important note]{.alert}
- `.fg` class for custom colors: [colored text]{.fg style="--col: #e64173"}
- `.bg` class for backgrounds: [highlighted text]{.bg style="--col: #e64173"}
- `.button` class for navigation: [[Next Section]{.button}](#next)

## 🛠 Local Development

To work on your presentation locally:

```bash
# Install Quarto (if not already installed)
# Visit https://quarto.org/docs/get-started/ for installation instructions

# Render the presentation
quarto render template.qmd

# Preview with live reload
quarto preview template.qmd
```

## 📁 Repository Structure

```
├── .github/workflows/
│   └── render-and-deploy.yml    # GitHub Actions workflow
├── _extensions/clean/            # Clean theme files
├── template.qmd                  # Main presentation file
├── _quarto.yml                   # Quarto project configuration
└── README.md                     # This file
```

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `b` | Toggle notes canvas for drawing |
| `c` | Open chalkboard for drawing |
| `s` | Speaker view with notes and timer |
| `r` | Toggle scroll view mode |
| `f` | Enter fullscreen mode |
| `o` | Overview of all slides |
| `?` | Show keyboard help |
| `Esc` | Exit current mode |

## 🔧 Advanced Configuration

### GitHub Actions Workflow

The included workflow (`.github/workflows/render-and-deploy.yml`) automatically:

1. Sets up Quarto and dependencies
2. Renders your presentation
3. Deploys to GitHub Pages

The workflow triggers on:
- Pushes to the main branch
- Pull requests to main
- Manual workflow dispatch

### Project Configuration

The `_quarto.yml` file contains project-wide settings. You can customize:

- Output directory
- Default format options
- Website metadata

### Multiplex Setup

To enable synchronized presentations across multiple devices:

1. **Edit your YAML frontmatter** in `template.qmd`:
```yaml
format:
  clean-revealjs:
    multiplex:
      url: 'https://reveal-multiplex.glitch.me/'
      secret: 'your-secret-key'  # For presenter
      id: 'your-presentation-id'
```

2. **For attendees** (view-only), remove the `secret` field:
```yaml
multiplex:
  url: 'https://reveal-multiplex.glitch.me/'
  id: 'your-presentation-id'
```

3. **Hosting**: You can use the free Glitch service or set up your own socket.io server.

## 📚 Resources

- [Quarto Documentation](https://quarto.org/docs/)
- [RevealJS Features](https://quarto.org/docs/presentations/revealjs/)
- [Clean Theme Documentation](https://github.com/grantmcdermott/quarto-revealjs-clean)

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📄 License

This template is based on the clean theme by Grant McDermott and is available under the MIT License.