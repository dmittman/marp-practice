# marp-practice

Sample product repository with a library of Marp presentations

## Overview

This repository contains a collection of [Marp](https://marp.app/) presentations about our product. Marp allows you to create beautiful slide decks using Markdown, and GitHub Actions automatically converts them to HTML that can be viewed on GitHub Pages.

## 📁 Repository Structure

```
.
├── presentations/          # Source Markdown files for presentations
│   ├── example-presentation.md
│   └── features-deep-dive.md
├── .github/
│   └── workflows/
│       └── marp-to-pages.yml  # GitHub Actions workflow
└── README.md
```

## 🚀 How It Works

1. **Create Presentations**: Add Marp-formatted Markdown files to the `presentations/` directory
2. **Automatic Build**: When changes are pushed to `main`, GitHub Actions automatically:
   - Converts all `.md` files in `presentations/` to HTML
   - Creates an index page listing all presentations
   - Deploys everything to GitHub Pages
3. **View Online**: Access your presentations at the GitHub Pages URL

## ✍️ Creating a New Presentation

1. Create a new `.md` file in the `presentations/` directory
2. Start with the Marp frontmatter:

```markdown
---
marp: true
theme: default
paginate: true
---

# Your Presentation Title

Your content here

---

## Slide 2

More content...
```

3. Commit and push to the `main` branch
4. GitHub Actions will automatically build and deploy your presentation

## 🎨 Marp Features

Marp supports many features including:
- Multiple themes (default, gaia, uncover)
- Pagination
- Custom CSS
- Image backgrounds
- Code syntax highlighting
- Math expressions (KaTeX)
- And much more!

Learn more at [Marp Documentation](https://marpit.marp.app/)

## 🧪 Testing Locally

To preview your presentations locally before committing:

1. Install Marp CLI:
```bash
npm install -g @marp-team/marp-cli
```

2. Convert a presentation to HTML:
```bash
marp presentations/example-presentation.md --html -o output.html
```

3. Open the generated HTML file in your browser

## 🔧 GitHub Pages Setup

To enable GitHub Pages for this repository:

1. Go to repository Settings → Pages
2. Under "Source", select "GitHub Actions"
3. The workflow will automatically deploy on the next push to `main`

## 📝 Notes

- Only `.md` files in the `presentations/` directory will be converted
- The workflow runs on pushes to `main` that affect presentation files
- You can also manually trigger the workflow from the Actions tab
- Built presentations are available at: `https://[username].github.io/[repository]/`

## 📄 License

This repository is licensed under the terms specified in the LICENSE file.
