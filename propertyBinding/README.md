# Prperty Binding

This repository contains practice code and interview Q&A based on concepts learned while studying Angular. The folder `Property Binding` includes hands-on examples demonstrating various property binding techniques in Angular.

---

## 📁 Folder: `Property Binding`

This folder contains:
- Examples of **property binding**
- Comparison between **interpolation** and **property binding**
- Usage of **image tags with property binding**
- Scenarios demonstrating **boolean attribute binding**
- Common **interview questions and answers**

---

## 🔍 Concepts Covered

### 🔹 Property Binding

Property binding allows setting DOM element properties using component values. It's useful when:
- Binding non-string values (like booleans, numbers, objects)
- Dynamically assigning paths (e.g., to an image tag)
- Toggling features via true/false

**Example:**
```html
<img [src]="imageUrl">
🔹 Interpolation vs Property Binding
Q1: What’s the difference between interpolation and property binding?
Answer:

Interpolation ({{ }}) always converts values to strings.

Property binding ([property]="value") binds the actual data type (boolean, number, object, etc.).

Interpolation	Property Binding
Always outputs a string	Preserves original data type
Good for text/labels	Good for dynamic element props

Example:

html
Copy
Edit
<!-- Interpolation -->
<img src="{{ imageUrl }}">

<!-- Property Binding -->
<img [src]="imageUrl">
🔹 Attribute Binding
Q2: Can you bind a DOM element’s attribute using property binding?
Answer:
Yes, use the attr. prefix for non-standard attributes.

Example:

html
Copy
Edit
<button [attr.aria-label]="ariaLabelText">Click me</button>
🔹 Boolean Attribute Binding
Q3: What happens if you use interpolation for boolean attributes?
Answer:
Interpolation treats booleans as strings ("true", "false"), which may break expected behavior.

Incorrect (interpolation):

html
Copy
Edit
<input type="checkbox" checked="{{ isChecked }}">
Correct (property binding):

html
Copy
Edit
<input type="checkbox" [checked]="isChecked">
🔹 Binding Multiple Properties
Q4: Can you bind multiple properties at once?
Answer:
Not in a single binding statement, but you can bind multiple properties individually on the same element.

Example:

html
Copy
Edit
<img [src]="imageUrl" [alt]="imageAlt" [width]="imgWidth" [height]="imgHeight">
✅ Summary
This repo is a personal learning space for mastering Angular fundamentals, with a focus on:

Clean, modular folder structure

Real interview preparation

Hands-on examples with actual Angular code

📌 Upcoming Topics
Event binding

Two-way data binding

Directives and structural bindings

Component communication

Routing and lazy loading