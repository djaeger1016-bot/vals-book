# VALS Book - Promotional Website

A website to promote the VALS book built with Hugo and automatically deployed to GitHub Pages.

## Getting Started

### Prerequisites
- [Hugo Extended](https://gohugo.io/installation/) (v0.87.0 or later)
- Git

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/djaeger1016-bot/vals-book.git
cd vals-book
```

2. Initialize the theme (if needed):
```bash
git submodule update --init --recursive
```

3. Start the Hugo development server:
```bash
hugo server -D
```

4. Open your browser to `http://localhost:1313`

### Building for Production

```bash
hugo
```

The static site will be built to the `public/` directory.

## Project Structure

```
vals-book/
├── .github/workflows/   # GitHub Actions deployment
├── config.toml          # Hugo configuration
├── content/             # Page content in Markdown
│   ├── _index.md        # Homepage
│   ├── about.md         # About the book
│   ├── chapters.md      # Chapter previews
│   └── contact.md       # Contact page
├── static/              # Static assets (images, downloads)
│   └── images/
├── themes/              # Hugo themes
└── layouts/             # Custom layouts (optional)
```

## Customization

### Update Site Information
Edit `config.toml` to customize:
- `title` - Your book title
- `baseURL` - Your GitHub Pages URL
- `params.author` - Author name
- `params.email` - Contact email
- Social media links

### Add Content
1. Edit markdown files in `content/` directory
2. Add images to `static/images/`
3. Changes automatically deploy to GitHub Pages on push to `main` branch

### Add a Theme
Choose from [Hugo Themes](https://themes.gohugo.io/):

```bash
git submodule add https://github.com/theNewDynamic/ananke.git themes/ananke
```

Then update `config.toml`:
```toml
theme = "ananke"
```

## Deployment

### Automatic GitHub Pages Deployment
The `.github/workflows/hugo.yml` workflow automatically:
1. Builds your Hugo site when you push to `main`
2. Deploys to GitHub Pages
3. Your site will be live at: `https://djaeger1016-bot.github.io/vals-book/`

### Enable GitHub Pages (if not already enabled)
1. Go to your repository Settings
2. Navigate to Pages (left sidebar)
3. Under "Build and deployment", select:
   - Source: **GitHub Actions**
4. Save

That's it! Future pushes will auto-deploy.

## Learn More
- [Hugo Documentation](https://gohugo.io/documentation/)
- [Hugo Themes Gallery](https://themes.gohugo.io/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

