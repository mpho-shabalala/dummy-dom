# UIComponents

A lightweight JavaScript library that provides a clean, modular interface for interacting with the DOM. The `UIComponents` class simplifies the creation, manipulation, and retrieval of common HTML elements, encapsulating native DOM operations into reusable methods.

---

## ✨ Features

- Create reusable HTML elements (`form`, `div`, `img`, `p`, `tr`, `td`, `li`, `header`, `button`, etc.) with optional attributes.
- Retrieve existing DOM elements using flexible attribute selectors.
- Validate element types and handle common DOM operation errors gracefully.
- Clean and extendable class-based design.

---

## 📦 Installation

Since this is a standalone class, simply import it into your JavaScript project:

```js
import UIComponents from './UIComponents.js';
```

---

## 🚀 Usage

```js
const ui = new UIComponents();

const form = ui.createForm('loginForm', 'form-class', 'POST');
document.body.appendChild(form);

const header = ui.createHeader('h2', 'Login Page', 'headerId', 'header-class');
form.appendChild(header);

const btn = ui.createButton('submitBtn', 'btn-primary', 'Submit');
form.appendChild(btn);
```

---

## 🧩 Methods

### Element Creation

| Method                                        | Description                         |
|----------------------------------------------|-------------------------------------|
| `createForm(id, className, method)`           | Creates a `<form>` element          |
| `createCard(id, className)`                   | Creates a custom `<card>` element   |
| `createLI(id, className)`                     | Creates an `<li>` list item         |
| `createTRow(id, className)`                   | Creates a table row (`<tr>`)        |
| `createTColumn(id, className)`                | Creates a table column (`<td>`)     |
| `createImg(src, alt, id, className)`          | Creates an `<img>` with attributes  |
| `createParagraph(textContent, id, className)` | Creates a `<p>` element             |
| `createDiv(id, className)`                    | Creates a `<div>` element           |
| `createHeader(type, text, id, className)`     | Creates a header (`<h1>` to `<h6>`) |
| `createButton(id, className, text)`           | Creates a `<button>` element        |

---

### DOM Selectors

| Method                                      | Description                                                   |
|--------------------------------------------|---------------------------------------------------------------|
| `getDomElement(elementType, id, className)` | Retrieves a DOM element by ID or class and validates its type |
| `getAllDomElements(className)`              | Returns a NodeList of all elements with the specified class   |

---

## 🔧 Internal Helpers

These are private methods used internally for validation and type checking.

- `#isNull()` – Validates if an attribute is `null`.
- `#isHeaderValid()` – Validates header tag types (`h1`–`h6`).
- `#isHTMLElementValid()` – Confirms element existence and correct tag type.

---

## ⚠️ Error Handling

The class will throw descriptive errors when:

- Required content is missing (e.g., button `textContent`)
- The specified element type is invalid
- The requested DOM element does not exist

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m "Add feature"`
4. Push to your branch: `git push origin feature-name`
5. Submit a pull request


