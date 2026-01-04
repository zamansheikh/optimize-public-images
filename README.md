# 🚀 Optimize Public Images

A powerful, interactive CLI tool to optimize images in your Next.js `public` folder. Convert images to WebP format with an intuitive selection interface and flexible optimization strategies.

## Features

✨ **Interactive Selection**

- Optimize all images at once
- Select by folder (and subfolders)
- Select individual files with checkboxes

🎯 **Flexible Strategies**

- **New Folder**: Create optimized copies in separate folders (customizable suffix)
- **Overwrite**: Place optimized WebP files alongside originals

🖼️ **Image Support**

- JPG, JPEG, PNG, GIF, SVG

🎨 **Professional UI**

- Colored terminal output
- Progress spinners
- Clear success/error reporting

## Installation

### As a Dev Dependency

```bash
npm install --save-dev optimize-public-images
```

Then run:

```bash
npx optimize-public
```

### As a Global Package

```bash
npm install -g optimize-public-images
```

Then run from any project:

```bash
optimize-public
```

## Usage

### Run the Interactive CLI

```bash
npx optimize-public
```

or globally:

```bash
optimize-public
```

### Help

```bash
optimize-public --help
```

## How It Works

1. **Scan**: Auto-detects your Next.js `public` folder
2. **Select**: Choose which images to optimize (all, by folder, or individual files)
3. **Configure**: Pick your strategy (new folder or overwrite)
4. **Optimize**: Converts images to WebP format with quality set to 80

### Example Folder Structure

**Before:**

```
public/
├── logo.png
├── images/
│   ├── hero.jpg
│   ├── card.png
│   └── icon.svg
└── icons/
    ├── home.png
    └── user.png
```

**After (New Folder Strategy with `_optimized` suffix):**

```
public/
├── logo.png
├── _optimized/
│   └── logo.webp
├── images/
│   ├── hero.jpg
│   ├── card.png
│   └── icon.svg
├── images_optimized/
│   ├── hero.webp
│   ├── card.webp
│   └── icon.webp
└── icons/
    ├── home.png
    └── user.png
```

(Note: SVG files are not converted to WebP; only raster images are optimized)

## Requirements

- Node.js 12.0+
- A Next.js project with a `public` folder

## Dependencies

- **sharp**: Image processing
- **glob**: File pattern matching
- **inquirer**: Interactive CLI prompts
- **chalk**: Colored terminal output
- **ora**: Loading spinners
- **fs-extra**: File system utilities

## Performance

Optimizing to WebP typically reduces image sizes by 25-35% compared to PNG/JPG.

## License

MIT

## Author

Your Name

## Support

For issues or feature requests, visit the GitHub repository.
