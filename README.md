# Ohmyfood - Restaurant Website

A mobile-first responsive website for a fictional restaurant booking service called "Ohmyfood". This project is built using HTML5 and SASS/CSS3 with a focus on responsive design and animations.  
**It includes automated build processes with `Git pre-commit hooks` to ensure compiled assets are always up-to-date.**

## Live Demo

[Ohmyfood](https://aladin002dz.github.io/ohmyfood-2025/)

## Features

- Mobile-first responsive design
- CSS animations using SASS
- BEM methodology for CSS class naming
- Pure CSS heart animation for favorites

## Project Structure

```
sass-tutorial/
├── css/
│   └── style.css
├── images/
│   └── (SVG and image files)
├── sass/
│   ├── _variables.scss
│   ├── _reset.scss
│   ├── _header.scss
│   ├── _hero.scss
│   ├── _functioning.scss
│   ├── _restaurants.scss
│   ├── _footer.scss
│   └── main.scss
├── index.html
└── README.md
```

## Getting Started

### Prerequisites

- Node.js
- npm

### Installation

1. Clone the repository
2. Install dependencies
   ```
   npm install
   ```

### Development

To work on the project with live SASS compilation:

```
npm run dev
```

### Build

To build the project for production:

```
npm run build
```

### Pre-commit Hook

This project includes a Git pre-commit hook that automatically builds the project and stages the compiled CSS files before each commit. The hook:

- Runs `npm run build` to compile SASS to CSS
- Automatically stages the `css/` directory to include compiled files in the commit

This ensures that the compiled CSS is always up-to-date and included in version control.

#### How to Set Up the Pre-commit Hook

1. **Navigate to the Git hooks directory:**

   ```bash
   cd .git/hooks/
   ```

2. **Create the pre-commit file:**

   ```bash
   touch pre-commit
   ```

3. **Make the file executable:**

   ```bash
   chmod +x .git/hooks/pre-commit
   ```

4. **Add the following content to the pre-commit file:**
   ```bash
   #!/bin/sh
   npm run build
   git add css/
   ```

#### How It Works

- The pre-commit hook runs automatically before every `git commit`
- It executes `npm run build` to compile your SASS files to CSS
- It then stages the compiled CSS files with `git add css/`
- If the build fails, the commit is prevented
- If the build succeeds, the commit proceeds with the updated CSS files

#### Manual Override

If you need to bypass the pre-commit hook for a specific commit, you can use:

```bash
git commit --no-verify
```

## Design Methodologies

- BEM (Block, Element, Modifier) methodology for CSS naming convention
- 7-1 pattern for SASS architecture (simplified)
- Mobile-first approach

## Resources

- [Sass Documentation](https://sass-lang.com/documentation)
- [BEM Methodology](https://getbem.com/)
