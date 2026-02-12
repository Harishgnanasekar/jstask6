#  JavaScript Array & String Methods – Complete Solutions

---

#  SECTION 1 – Array Higher Order Methods

---

##  Task 1 – forEach()

```javascript
let subjects = ["Maths", "Science", "English", "History"];

let result;
result = subjects.forEach((subject, index) => {
  console.log(`Subject ${index + 1}: ${subject}`);
});

console.log("Return value:", result); // undefined
```

**Why forEach() returns undefined?**
Because `forEach()` only executes a function for each element. It does NOT return a new array.

---

##  Task 2 – map()

```javascript
let prices = [100, 200, 300, 400];

let newPrices = prices.map(price => price + price * 0.10);

console.log(newPrices); 
// [110, 220, 330, 440]
```

---

##  Task 3 – filter()

```javascript
let students = [
 { name: "A", marks: 45 },
 { name: "B", marks: 75 },
 { name: "C", marks: 35 },
 { name: "D", marks: 85 }
];

let passedStudents = students.filter(student => student.marks > 50);

console.log(passedStudents);
```

---

##  Task 4 – find()

```javascript
let firstTopper = students.find(student => student.marks > 50);

console.log(firstTopper);
```

**Difference between filter() and find():**

* `filter()` → returns ALL matching elements (array)
* `find()` → returns ONLY FIRST matching element (object)

---

##  Task 5 – reduce()

```javascript
let cart = [
 { item: "Shirt", price: 1000 },
 { item: "Shoes", price: 2000 },
 { item: "Watch", price: 3000 }
];

let total = cart.reduce((sum, item) => sum + item.price, 0);

let totalWithTax = cart.reduce((sum, item) => sum + item.price * 1.05, 0);

console.log("Total:", total);
console.log("Total with 5% tax:", totalWithTax);
```

---

##  Task 6 – some()

```javascript
let numbers = [1, 3, 5, 7, 8];

let hasEven = numbers.some(num => num % 2 === 0);

console.log(hasEven); // true
```

---

##  Task 7 – every()

```javascript
let ages = [22, 25, 19, 30];

let allAdults = ages.every(age => age > 18);

console.log(allAdults); // true
```

---

##  Task 8 – sort()

```javascript
let salaries = [50000, 10000, 70000, 30000];

// Ascending
salaries.sort((a, b) => a - b);
console.log("Ascending:", salaries);

// Descending
salaries.sort((a, b) => b - a);
console.log("Descending:", salaries);
```

**Why normal sort() fails?**
Because it sorts numbers as strings (alphabetical order).

---

##  Task 9 – Array Conversion

```javascript
let arr = [10, 20, 30, 40];

console.log(arr.toString()); 
// "10,20,30,40"

console.log(arr.join("-"));  
// "10-20-30-40"
```

---

#  SECTION 2 – String Methods

---

##  Task 10 – charAt() & charCodeAt()

```javascript
let word = "Developer";

console.log(word.charAt(4));      // l
console.log(word.charCodeAt(4));  // 108
```

---

##  Task 11 – slice()

```javascript
let company = "StacklyCompany";

let result = company.slice(8);
console.log(result); // Company
```

---

##  Task 12 – Case Conversion

```javascript
let userInput = "javaScript";

console.log(userInput.toUpperCase());
console.log(userInput.toLowerCase());
```

---

##  Task 13 – trim()

```javascript
let email = "   naveen@gmail.com   ";

console.log(email.trim());
```

---

##  Task 14 – includes()

```javascript
let message = "Welcome to JavaScript Training";

console.log(message.includes("JavaScript")); // true
```

---

##  Task 15 – split()

```javascript
let movie = "spider-man-no-way-home";

let movieArray = movie.split("-");

console.log(movieArray);
```

---

##  Task 16 – indexOf() & lastIndexOf()

```javascript
let text = "programming";

console.log(text.indexOf("m"));      // 6
console.log(text.lastIndexOf("m"));  // 7
```

---

##  Task 17 – replace()

```javascript
let tech = "I love python";

let updated = tech.replace("python", "javascript");

console.log(updated);
```

---

##  Task 18 – startsWith() & endsWith()

```javascript
let filename = "report.pdf";

console.log(filename.startsWith("report")); // true
console.log(filename.endsWith(".pdf"));     // true
```

---

##  Task 19 – repeat()

```javascript
let star = "*";

console.log(star.repeat(10)); 
// **********
```

---

#  FINAL TEAM CHALLENGE – Employee Report System

```javascript
let employees = [
 { name: "Naveen", salary: 50000 },
 { name: "Arun", salary: 30000 },
 { name: "Kiran", salary: 70000 }
];

// Convert names to uppercase
let upperNames = employees.map(emp => ({
  ...emp,
  name: emp.name.toUpperCase()
}));

// Filter salary > 40000
let highSalary = employees.filter(emp => emp.salary > 40000);

// Find first salary > 60000
let firstHigh = employees.find(emp => emp.salary > 60000);

// Total salary
let totalSalary = employees.reduce((sum, emp) => sum + emp.salary, 0);

// Sort descending
let sorted = [...employees].sort((a, b) => b.salary - a.salary);

console.log("Uppercase Names:", upperNames);
console.log("Salary > 40000:", highSalary);
console.log("First > 60000:", firstHigh);
console.log("Total Salary:", totalSalary);
console.log("Sorted Desc:", sorted);
```

