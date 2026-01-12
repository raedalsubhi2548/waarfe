# Waarfe Twilight Theme 🌌

A premium, futuristic "Galaxy / Orbit" UI theme for Salla, designed with an Arabic-first RTL approach.

## Brand Identity
- **Primary Color**: Deep Emerald (`#09382e`)
- **Secondary Color**: Soft Gold (`#d7c676`)
- **Background**: Space Black-Green (`#0b1412`)
- **Typography**: Tajawal (Arabic/Latin)

## Structure
- `src/assets/styles/_variables.scss`: Design tokens (Colors, Typography, Spacing).
- `src/assets/styles/home.scss`: Specific styles for Hero and Orbit sections.
- `src/assets/styles/app.scss`: Main entry point, imports fonts and global styles.
- `src/views/index.twig`: Homepage content.
- `src/views/partials/`: Header and Footer components.

## Customization

### 1. Changing Colors
Edit `src/assets/styles/_variables.scss`. 
Example: To change the primary glow, update `--color-glow`.

### 2. Modifying the Orbit Services
The orbit system is in `src/views/index.twig` inside `.orbit-ring`.
- To add a service, duplicate a `.planet` block.
- **Important**: If you change the number of planets from 8, you must update the SCSS loop in `src/assets/styles/home.scss`:
  ```scss
  @for $i from 1 through 8 { ... } // Change 8 to your new count
  ```
  And adjust the rotation angle `360 / count`.

### 3. Editing Text
All text content is currently hardcoded in `src/views/index.twig` (Homepage) and partials. For a real Salla theme, these should be converted to `{{ trans('key') }}` or theme settings.

## Development
- Ensure you compile SCSS to CSS using your build tool (Webpack/Vite/Gulp).
- The theme expects `assets/styles/app.css` to be generated.
