# Code Style Guide for Frontend (HTML, CSS, JavaScript)

**Source of Style Guide:**
- [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
- [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)
- [MDN Web Docs Best Practices](https://developer.mozilla.org/)

---

## 1. General Principles
- Code must be **readable, maintainable, and consistent**.
- Use **meaningful variable names** and **clear indentation**.
- Include **comments** explaining logic for non-trivial code sections.
- Avoid duplication and keep functions **modular and reusable**.
- Keep line length ≤ 100 characters for readability.

---

## 2. HTML Style Guide
- File extension: `.html`
- Use lowercase tag names (`<div>`, `<p>`, `<section>`, etc.).
- Indentation: **2 spaces per level**.
- Use **semantic HTML5 tags** (`<header>`, `<main>`, `<footer>`, `<article>`) when possible.
- Attribute order should follow:
  1. `id`
  2. `class`
  3. `name`
  4. `data-*`
  5. `src`, `href`
  6. `title`, `alt`
- All attribute values must be **quoted**.
- Avoid inline styles and JavaScript; link CSS and JS files externally.
- Add descriptive comments to separate main sections.
## 3. CSS Style Guide
- File extension: .css
- Follow the BEM naming convention (Block–Element–Modifier) for clarity:
```
.contact-card__name { ... }
.contact-card__button--delete { ... }
```
- Use 2 spaces for indentation.
- Always include a space after a colon and before {:
```
h1 {
  color: #333;
  font-size: 20px;
}
```
- Group related selectors together.
- Prefer using relative units (em, rem, %) over absolute (px) for responsive design.
- Use CSS variables or a separate colors section for consistent theme colors.
- Add comments for each major section.
- Avoid IDs in selectors unless necessary; use classes instead.
- End each rule with a semicolon ;.
## 4. Javascript Style Guide
- File extension: .js
- Follow ES6 (ECMAScript 2015) syntax.
- Use const and let — avoid var.
- Use camelCase for variables and functions:
```
const contactList = [];
function addContact(name, email, phone) { ... }
```
- Use PascalCase for class names:
```
class ContactManager { ... }
```
- Indentation: 2 spaces per level.
- Always include semicolons at the end of statements.
- Use template literals instead of string concatenation:
```
const message = `Contact ${name} added successfully.`;
```
- Add inline comments using // for short notes, and block comments (/* ... */) for detailed explanations.
- Handle API calls asynchronously using async/await and include error handling:
```
try {
  const response = await fetch(API_URL);
} catch (error) {
  console.error('Error fetching contacts:', error);
}
```
- Avoid global variables; wrap code in functions or modules.
- Use strict equality (=== and !==) instead of loose equality (==, !=).
- Keep functions short and focused on one task.
## 5. File Naming Conventions
- Use lowercase letters and hyphens for filenames.
Example:
```
index.html
style.css
script.js
```
- Do not include spaces in filenames.
## 6. Commenting Conventions
- Comments should be concise but informative.
- Use TODO/FIXME annotations for unfinished or questionable code:
```
// TODO: Add input validation for phone number
```
- In HTML and CSS, use section headers to organize related content.
## 7. Linting and Formatting
- Use Prettier for automatic formatting.
- Use ESLint with the Airbnb configuration for JavaScript linting.
- Run a linter before committing to ensure consistent code style.
