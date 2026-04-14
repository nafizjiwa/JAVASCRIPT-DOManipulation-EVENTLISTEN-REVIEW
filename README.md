# JAVASCRIPT-DOM-MAN-EVENT-LISTENER-REVIEW
---

# **DOM & JavaScript Events**

### **APIs & Web APIs**
- **API**: Rules that let software communicate.
- **Web APIs**: APIs for the browser environment.
  - **Browser APIs**: Built into the browser (DOM, window, navigator).
  - **Third‑Party APIs**: External services (ex: Google Maps).

---

### **DOM Basics**
- **DOM (Document Object Model)**: Tree structure representing HTML.
- **Root node**: `<html>`.
- **Parent node**: Contains other elements.
- **Child node**: Element inside another element.

---

### **Browser Interfaces**
- **navigator**: Info about browser, OS, user agent.
- **window**: Represents browser window; controls navigation, size, etc.

---

# **DOM Selection Methods**
### **getElementById()**
- Selects **one** element by unique ID.

### **querySelector()**
- Selects the **first** element matching a CSS selector.

### **querySelectorAll()**
- Selects **all** matching elements; returns a NodeList.

---

# **Working With Content**
### **innerHTML**
- Sets/gets HTML markup inside an element.

### **createElement()**
- Creates a new DOM element.

### **innerText**
- Returns **visible** text only.

### **textContent**
- Returns **all** text, including hidden text.

---

# **Adding & Removing Elements**
### **appendChild()**
- Adds a node to the end of a parent’s children.

### **removeChild()**
- Removes a specific child node from the DOM.

---

# **Attributes**
### **setAttribute()**
- Adds or updates an attribute on an element.

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

Just tell me the format you want.
