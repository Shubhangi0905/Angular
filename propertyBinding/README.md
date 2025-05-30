# 📁 Property Binding in Angular

This directory contains Angular examples that demonstrate the concept of **Property Binding**, including its usage with various HTML elements and a comparison with interpolation.

---

###This folder contains:

- Examples of **property binding**
- Comparison between **interpolation** and **property binding**
- Usage of **image tags with property binding**
- Scenarios demonstrating **boolean attribute binding**
- Common **interview questions and answers**

## 🧠 Key Concepts

### Interpolation (`{{ }}`)

- Used to bind component data to the template.
- Automatically converts data to strings.

**Example:**

<pre>```html
<p>{{ userName }}</p>```</pre>

### Property Binding ([ ])

Property binding allows setting DOM element properties using component values. It's useful when:
- Binding non-string values (like booleans, numbers, objects)
- Dynamically assigning paths (e.g., to an image tag)
- Toggling features via true/false
  
**Example:**

<pre>```html
<button [disabled]="isDisabled">Submit</button>```</pre>

##Binding with <img> Tags

-Demonstrates dynamic binding of image sources.

**Example:**

<pre>```html
<img [src]="imageUrl" alt="Dynamic Image">```</pre>

##❓ Interview Questions & Answers

**1. What is the difference between interpolation and property binding?**

Answer:

Interpolation ({{ }}) is used to bind data to the template and always converts the data to a string. Property binding ([ ]) binds data to DOM properties and preserves the data type. For instance, binding a boolean value should use property binding to maintain its boolean nature.

**2. Can you bind a DOM element's attribute using property binding?**

Answer:

Yes. You can bind attributes using the attr. prefix in property binding.

Example:

<pre>```html
<button [attr.aria-label]="ariaLabelText">Click me</button>```</pre>

This binds the aria-label attribute to the ariaLabelText property in the component.

**3. What happens if you use interpolation instead of property binding for a boolean attribute?**

Answer:

Using interpolation for boolean attributes converts the value to a string, which may not have the desired effect.

<pre>```Incorrect:

html
<!-- 'true' is a string -->
<button disabled="{{ isDisabled }}">Submit</button>
Correct:

html
<!-- isDisabled is a boolean -->
<button [disabled]="isDisabled">Submit</button>```</pre>

In the incorrect example, the button may not behave as expected because the disabled attribute receives a string instead of a boolean.

**4. Can you bind multiple properties at once? If so, how?**

Answer:

While you can't bind multiple properties simultaneously in a single statement, you can bind multiple properties individually on the same element.

Example:

<pre>```html
<input [value]="userName" [disabled]="isDisabled" [attr.maxlength]="maxLength" />```</pre>

Each property is bound separately, allowing for dynamic and flexible templates.

##✅ Summary

This repo is a personal learning space for mastering Angular fundamentals, with a focus on:

-Clean, modular folder structure
-Real interview preparation
-Hands-on examples with actual Angular code

##📌 Upcoming Topics

-Event binding
-Two-way data binding
-Directives and structural bindings
-Component communication
-Routing and lazy loading


