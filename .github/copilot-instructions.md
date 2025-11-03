# AI Assistant Instructions for Sacred Union Project

## Project Overview
Sacred Union is a web-based platform for couples' spiritual development and relationship enhancement, built with HTML, CSS, and vanilla JavaScript. The project follows a component-based architecture with modular sections that can be included in different pages.

## Project Structure
- **Root HTML Files**: Main entry points (`index.html`, `start.html`, `course.html`, etc.)
- **CSS Organization**: 
  - `css/styles.css`: Global styles and shared components
  - `css/course.css`: Course-specific styles
  - `css/start.css`: Start page specific styles
- **Sections**: Reusable HTML components in `sections/` directory
- **Assets**: Images stored in `images/` directory

## Key Design Patterns

### 1. Component Architecture
- Components are stored in `sections/` and included where needed
- Each component is self-contained with its HTML, styles, and scripts
- Example components: `navbar.html`, `hero.html`, `modules.html`

### 2. CSS Conventions
- Base font size: `html { font-size: 60%; }` (1rem = 10px)
- Colors:
  - Primary: `#D21117` (red)
  - Secondary: `#7BC3FF` (blue)
  - Text: `#4B4E53` (gray)
- Font stack:
  ```css
  font-family: "DM Sans", sans-serif;  // Primary
  font-family: "Source Serif Pro", serif;  // Secondary
  font-family: "Inter", sans-serif;  // Body text
  ```

### 3. Modal Pattern
Used for interactive components (e.g., module details). Standard structure:
```html
<div class="modal">
  <div class="modal-content">
    <h2 id="modalTitle">Title</h2>
    <p id="modalDescription">Description</p>
    <button class="close-btn">Close</button>
  </div>
</div>
```

### 4. Animation Conventions
- Fade animations use consistent timing:
  ```css
  animation: fadeInUp 1.5s ease forwards;
  transition: all 0.3s ease;
  ```
- Interactive elements use transform scale on hover:
  ```css
  transform: scale(1.05);
  ```

### 5. Responsive Layout
- Uses rem units for consistent scaling
- Flexbox for component layout
- Grid system for module layouts

## Development Workflow

### Adding New Pages
1. Create HTML file in root directory
2. Include necessary sections from `sections/`
3. Link appropriate CSS files
4. Add page-specific scripts at bottom

### Creating New Components
1. Create component HTML in `sections/`
2. Add component-specific styles to appropriate CSS file
3. Include component script if needed
4. Import into main pages as needed

## Common Patterns to Follow
1. Use lowercase for all filenames and HTML elements
2. Include interactive elements' scripts at bottom of HTML files
3. Follow established spacing and padding patterns
4. Maintain consistent color scheme and typography
5. Use existing modal pattern for pop-up content

## Integration Points
- External Libraries:
  - Typed.js for animated text (`typed.js@2.0.12`)
  - Google Fonts for typography
- No backend integration currently - static site structure