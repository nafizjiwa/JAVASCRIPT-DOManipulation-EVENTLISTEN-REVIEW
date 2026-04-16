# JAVASCRIPT-DOM/MAN-EVENT-LISTENER-REVIEW
---

# **DOM & JavaScript Events**

### **APIs & Web APIs**
- **API**: (Application Programming Interface) Rules that let software communicate with each toher.
- **Web APIs**: APIs for the browser or the web.
  - **Browser APIs**: Built into the browser (DOM, window, navigator).
  - **Third‑Party APIs**: retrieve code from external services (ex: Google Maps).
---

### **DOM Basics**
- Programming interface to interact with HTML documents
- **DOM (Document Object Model)**: Tree structure representing HTML.
  - **Root node**: `<html>` element or top level container.
  - Desendents of the root
    - **Parent node**: Contains other elements.
    - **Child node**: Element inside another element.
---

### **Browser Interfaces**
- **navigator interface**: Info about browser, OS, user agent.
- **window interface**: Represents browser window; controls navigation, size, etc.
---

# **DOM Selection Methods**
    ### **getElementById()**
    - Selects and returns **one** element by unique ID.
    
    ### **querySelector()**
    - Selects and returns the **first** element matching a CSS selector.
    
    ### **querySelectorAll()**
    - Selects and returns **all** matching elements in a NodeList.
---

# **Working With Content**
### **innerHTML( )**
- Sets/gets HTML markup inside an element.

### **createElement()**
- Creates a new DOM element.

### **innerText**
- Returns **visible** text of chosen element and its descendents.

### **textContent**
- Returns **all** text Content as it appears in DOM, including hidden text.
---

# **Adding & Removing Elements**
### **appendChild()**
- Adds a node to the -END- of a parent’s children.

      <ul id="desserts">
        <li>Cake</li>
        <li>Pie</li>
      </ul>
      
      const dessertsList = document.getElementById("desserts");
      const listItem = document.createElement("li");

      listItem.textContent = "Cookies";
      dessertsList.appendChild(listItem);
---

### **removeChild()**
- Removes a specific child node from the DOM.

# **Attributes**
### **setAttribute(attributeName, attributeValue)**
- Adds or updates an attribute on an element.
- AttributeNames  - class, id, src, href, lt, data-user
---

# **Events & Event Object**
- **Event object**: Contains details about the triggered event.
- `.type` shows event type (e.g., `"click"`).
---

# **Event Listeners**
### **addEventListener()**
- Listens for events (click, input, change, etc.).

### **removeEventListener()**
- Removes a previously attached listener.

### **Inline Handlers**
- `<button onclick="...">`  
- Not best practice; use addEventListener instead.

---

# **Specific Events**
### **change Event**
- Fires when input value changes (select, checkbox, radio, etc.).

---

# **Event Flow**
### **Event Bubbling**
- Event travels **from child → parent**.

### **stopPropagation()**
- Stops the event from bubbling further.

---

# **Event Delegation**
- Attach one listener to a **parent** to handle events from **multiple children**.
- Efficient for dynamic content.

---

# **📌 DOMContentLoaded**
- Fires when **HTML is fully loaded and parsed**.
- Does **not** wait for images, stylesheets, or external resources.
- Useful for safely running JS that touches the DOM.

---

# **📌 Working with `style` and `classList`**

### **Element.style**
- Accesses or sets **inline styles**.
- Example:  
  ```js
  paraEl.style.color = "red";
  ```

### **Element.classList**
- Add, remove, or toggle CSS classes.
- Methods:  
  - `.add("class")`  
  - `.remove("class")`  
  - `.toggle("class")`
- Example toggle:
  ```js
  toggleBtn.addEventListener("click", () => menu.classList.toggle("show"));
  ```

---

# **📌 setTimeout()**
- Runs code **once after a delay**.
- Example:
  ```js
  setTimeout(() => console.log("Runs after 3s"), 3000);
  ```

# **📌 setInterval()**
- Runs code **repeatedly** at fixed intervals.
- Use `clearInterval()` to stop it.
- Example:
  ```js
  const id = setInterval(() => console.log("Tick"), 1000);
  setTimeout(() => clearInterval(id), 5000);
  ```

---

# **📌 requestAnimationFrame()**
- Schedules animation updates **before the next screen repaint**.
- Produces smoother animations than `setInterval`.
- Example loop:
  ```js
  function animate() {
    update();
    requestAnimationFrame(animate);
  }
  ```

---

# **📌 Web Animations API**
- Create animations directly in JS.
- Supports duration, easing, direction, iterations, etc.
- Example:
  ```js
  square.animate(
    [{ transform: 'translateX(0)' }, { transform: 'translateX(100px)' }],
    { duration: 2000, iterations: Infinity, direction: 'alternate' }
  );
  ```

---

# **📌 Canvas API**
- Used for drawing shapes, text, images, and graphics.
- Requires a `<canvas>` element and a rendering context.
- Example:
  ```js
  const ctx = canvas.getContext('2d');
  ctx.fillStyle = 'crimson';
  ctx.fillRect(1, 1, 150, 100);
  ```

---

# **📌 Dialogs & Modals (`<dialog>` element)**

### **Modal vs Non‑Modal**
- **Modal**: blocks interaction with the rest of the page.
- **Non‑modal**: allows interaction with the page behind it.

### **Open a modal**
```js
dialog.showModal();
```

### **Open a non‑modal dialog**
```js
dialog.show();
```

### **Close a dialog**
```js
dialog.close();
```
---


