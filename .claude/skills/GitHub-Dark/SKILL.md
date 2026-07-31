```markdown
# GitHub-Dark Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and workflows used in the GitHub-Dark repository, a JavaScript project for generating and maintaining dark-themed user CSS for GitHub. You'll learn about the project's coding conventions, automated CSS regeneration, release management, and testing patterns.

## Coding Conventions

- **File Naming:**  
  Uses `camelCase` for JavaScript files.  
  _Example:_  
  ```
  githubDarkTheme.js
  cssGenerator.js
  ```

- **Import Style:**  
  Uses relative imports for modules.  
  _Example:_  
  ```js
  import utils from './utils';
  import cssVars from '../styles/cssVars';
  ```

- **Export Style:**  
  Uses default exports for modules.  
  _Example:_  
  ```js
  export default function generateCSS(options) {
    // ...
  }
  ```

- **Commit Messages:**  
  Freeform messages, sometimes prefixed with `fix`.  
  _Example:_  
  ```
  fix: correct button color in dark mode
  update font settings for headings
  ```

## Workflows

### Automated CSS Regeneration
**Trigger:** When source files or configuration change  
**Command:** `/regenerate-css`

1. Detect changes in source or config files.
2. Run the CSS generation script or workflow.
3. Overwrite or update `github-dark.user.css` (and sometimes related CSS files).
4. Commit the regenerated CSS file(s).

_Example:_  
```bash
# Detect changes and regenerate CSS
npm run build-css

# Commit the changes
git add github-dark.user.css
git commit -m "regenerate CSS after theme update"
```

### Release Version Bump and Bundle
**Trigger:** When a new version is ready to be released  
**Command:** `/release`

1. Update the version in `package.json`.
2. Regenerate CSS files (`github-dark.user.css`, `github-custom-fonts.user.css`).
3. Commit the updated `package.json` and CSS files.

_Example:_  
```bash
# Bump version (using npm or manually)
npm version minor

# Regenerate CSS
npm run build-css

# Commit all updated files
git add package.json github-dark.user.css github-custom-fonts.user.css
git commit -m "release: v1.2.0 and bundle updated CSS"
```

## Testing Patterns

- **Test File Pattern:**  
  Test files follow the `*.test.*` naming convention.  
  _Example:_  
  ```
  cssGenerator.test.js
  themeUtils.test.js
  ```

- **Framework:**  
  The testing framework is unknown, but tests are likely JavaScript-based and colocated with source files.

## Commands

| Command         | Purpose                                             |
|-----------------|-----------------------------------------------------|
| /regenerate-css | Regenerate the user CSS file(s) after source changes|
| /release        | Prepare a new release and bundle regenerated CSS    |
```
