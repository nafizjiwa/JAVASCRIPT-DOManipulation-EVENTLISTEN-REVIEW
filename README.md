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
      //Select parent
      const dessertsList = document.getElementById("desserts");
      //Create child list
      const listItem = document.createElement("li");

      //add text to child
      listItem.textContent = "Cookies";
      //append child to parent
      dessertsList.appendChild(listItem);
---

### **removeChild()**
- Removes a specific child node from the DOM.

# **Attributes**
### **setAttribute( )**
- **setAttribute(attributeName, attributeValue)**
- Adds or updates an attribute on an element.
- AttributeNames  - class, id, src, href, lt, data-user
---

# **Events & Event Object**
- **Event object**: Contains details (payload) about the triggered event.
- `.type` shows event type in all event objects (e.g., `"click"`).
---

# **Event Listeners**
### **addEventListener(eventToListenFor, functionToRunWhenEventOccurs)**
- Listens for events (click, input, change, etc.).
- Calls a function when event triggered

### **removeEventListener()**
- Removes a previously attached listener.
- Calls a function when event triggered

### **Inline Handlers**
- Attributes on HTML elements to execute JS when event occurs
- `<button onclick="...">`  
- Not best practice; use addEventListener instead.

---

# **TYPES OF EVENTS**
### **change Event**
- Fires when INPUT VALUE CHANGED BY USER (select, checkbox, radio, etc.).

---

# **Event Flow**
### **Event Bubbling**
- Event travels OR BUBBLES UP**from child → parent**.

### **stopPropagation()**
- Stops the event from bubbling further.

---
# **Event Delegation**
- Listening to events that have bubbled up to a parent
- Attach one listener to a **parent** to handle events from **multiple children**.

---
# **📌 DOMContentLoaded**
- Fires when **HTML document is fully loaded and parsed**.
- Does **not** wait for images, stylesheets, or external resources.

---

# **📌 Working with `style` and `classList` PROPERTIES**

### **Element.style**
- Gets or sets **inline styles OF AN ELEMENT**.
- Ex:  
  ```js
  paraEl.style.color = "red";
  ```

### **Element.classList**
- Add, remove, or toggle CSS classes.
- Methods:  
  - `element.classList.add("class")`  
  - ``element.classList.remove("class")`  
  - ``element.classList.toggle("class")`
- Example toggle:
  ```js
  toggleBtn.addEventListener("click", () => menu.classList.toggle("show"));
  ```
---
# **📌 setTimeout(functionToRun, runFunctionAfterThisMuchTimeHasPassed)**
- Runs code **once after a delay**.
- Example:
  ```js
  setTimeout(() => console.log("Runs after 3s"), 3000);
  ```

# **📌 setInterval(functionToRun, runFunctionEverySoManySeconds)**
- Runs code **repeatedly** at fixed intervals.
- Use `clearInterval()` to stop it.
- Example:
  ```js
  const ID = setInterval(() => console.log("Tick"), 1000);
  setTimeout(() => clearInterval(ID), 5000);
  ```

---
# **📌 requestAnimationFrame()**
- Schedules an animation update **before the next screen repaint(Browser Refresh)**.
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
- CREATE ANIMATIONS DIRECTLY IN JS.
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
- A TOOL TO CONTROL GRAPHICS INSIDE JS r drawing shapes, text, images, and graphics.
- Requires a `<canvas>` element in HTML.
- Example:
  ```js
  const ctx = canvas.getContext('2d');   //draw in 2D
  ctx.fillStyle = 'crimson';             //set background
  ctx.fillRect(1, 1, 150, 100);          //Draw a rectangle
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


