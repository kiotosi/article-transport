# Article Transport

> **Note**
> This project is being developed as a pet project for my blog.

**Article Transport** is a utility to translate text from markdown into different formats.

These formats include:
- HTML
- Plain Text
- Extended Markdown for Nuxt Content
- JSON
- XML

# Build steps

# Use \[tl;dr\]

**Basic syntax**:
```sh
art --[template-language] [file]

# or

art --to=[template-language] [file]
```

## Basic converting
**Convert markdown to HTML**:
```bash
art --html index.md
```

**Convert markdown to Plain text**:
```bash
art --text index.md
```

**Convert markdown to JSON**:
```bash
art --json index.md
```

**Convert markdown to XML**:
```bash
art --xml index.md
```

## Convert Markdown to HTML with specific config

> **Note**
> Default name for config - `.artrc.toml`

**Config example**:

```toml
# Describe classes for specific elements
[class]
heading1 = 'title'
heading2 = 'sub-title'
heading3 = 'sub-sub-title'
heading4 = 'quad-title'
heading5 = 'xs-title'
heading6 = 'mini-title'
paragraph = 'text'
quote = 'q'

# Set config for HTML
[config]
generateBoilerplate = false
outputDirectory = 'dist'

# Additional files
[template]
header = 'templates/header.html' # You can paste here XML, Markdown and HTML files
footer = 'templates/footer.html'
```

**Choose specific config and generate HTML**:
```bash
art --config=./artrc.html.toml --html index.md
```