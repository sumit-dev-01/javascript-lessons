# Practical JavaScript Tasks for Students

## **Task 1: Selecting Elements Using NodeList and Array**

### **Objective:**  
Learn how to **select elements using `querySelectorAll()`**, convert a **NodeList into an array**, and access elements using indexing.

### **Steps:**  
1. Create an HTML file with at least **5 paragraphs (`<p>`)** inside a `<div class="content">`.
2. Use `document.querySelectorAll(".content p")` to select all `<p>` elements.
3. Convert the NodeList into an array using `Array.from()`.
4. Use **indexing** to access and modify the third `<p>` element's text using `.innerText`.

### **Example Code:**
```javascript
let paragraphs = document.querySelectorAll(".content p");
let paraArray = Array.from(paragraphs);
paraArray[2].innerText = "Updated third paragraph!";
console.log(paraArray[2].innerText);
```

### **Bonus Challenge:**  
- Try **iterating** through the converted array and changing the text color of all paragraphs.

---

## **Task 2: Updating Elements Dynamically Using NodeList**

### **Objective:**  
Learn how to **dynamically update text** inside a class element selected using NodeList.

### **Steps:**  
1. Create an HTML file with a `<ul class="items">` containing at least **4 `<li>` elements**.
2. Select all `<li>` elements using `querySelectorAll(".items li")`.
3. Update the **second `<li>` element** dynamically using `.innerText`.

### **Example Code:**
```javascript
let listItems = document.querySelectorAll(".items li");
listItems[1].innerText = "Updated Second Item!";
```

### **Bonus Challenge:**  
- Try **looping** through the list and appending text dynamically.

---

## **Task 3: Adding a New Element After a Selected Element**

### **Objective:**  
Learn how to **add a new element dynamically** after an existing NodeList element.

### **Steps:**  
1. Create an HTML file with a `<div class="container">` and at least **3 `<h2>` elements**.
2. Select all `<h2>` elements using `querySelectorAll(".container h2")`.
3. Create a new `<h2>` element and insert it **after the second `<h2>`**.

### **Example Code:**
```javascript
let headings = document.querySelectorAll(".container h2");
let newHeading = document.createElement("h2");
newHeading.innerText = "New Heading Inserted";
headings[1].insertAdjacentElement("afterend", newHeading);
```

### **Bonus Challenge:**  
- Try changing the **text color** of all `<h2>` elements after insertion.

---

## **Task 4: Removing Specific Elements from a NodeList Dynamically**

### **Objective:**  
Learn how to **remove elements** from the DOM using `remove()` and understand the difference between **modifying a NodeList vs modifying the DOM**.

### **Steps:**  
1. Create a `<ul class="student-list">` with at least **5 `<li>` items** inside.
2. Select all `<li>` elements using `querySelectorAll(".student-list li")`.
3. Remove the **third `<li>` element** dynamically using `.remove()`.
4. Log the **NodeList length before and after removal** to check if the NodeList updates dynamically.

### **Example Code:**
```javascript
let students = document.querySelectorAll(".student-list li");

console.log("Total students before:", students.length);
students[2].remove();  // Remove the third student
console.log("Total students after:", students.length);  // Check if it updates
```

### **Bonus Challenge:**  
- Try adding a new `<li>` dynamically **after removal** and observe if `querySelectorAll()` updates automatically.
- Use `Array.from(students).forEach()` to iterate and modify all items after deletion.

---
