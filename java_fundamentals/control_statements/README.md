# 🔀 Control Statements

## 🧠 1. Why + Definition

### ❓ Problem

Without control statements:

- Code executes **linearly (top to bottom)**
- No decision-making capability
- Cannot handle real-world scenarios like validation, branching, or conditions

👉 Real systems require **decision-making at every step**

---

### 📌 Definition

Control statements allow a program to:

- Execute different blocks of code based on conditions
- Control the flow of execution

---

### 🌍 Real-world Analogy

Traffic system:

- Green → go
- Red → stop
- Yellow → wait

👉 Program flow changes based on conditions, just like signals.

---

## 💻 2. Syntax and Implementation

### ✅ Basic `if`

```java id="cs1"
if(age >= 18) {
    System.out.println("Eligible to vote");
}
```

---

### 🔁 `if-else`

```java id="cs2"
if(age < 18) {
    System.out.println("Minor");
} else {
    System.out.println("Adult");
}
```

---

### 🔀 `if-else-if` Ladder

```java id="cs3"
if(marks > 90) {
    grade = "A";
} else if(marks > 75) {
    grade = "B";
} else {
    grade = "C";
}
```

---

### ⚡ `switch` Statement

```java id="cs4"
switch(day) {
    case 1: System.out.println("Monday"); break;
    case 2: System.out.println("Tuesday"); break;
    default: System.out.println("Invalid");
}
```

---

### ⚠️ Wrong Implementation (Common Mistakes)

#### ❌ Assignment Instead of Comparison

```java id="cs5"
if(age = 18) { } // ❌
```

---

#### ❌ Missing Braces

```java id="cs6"
if(age > 18)
    System.out.println("Adult");
    System.out.println("Eligible"); // always runs ❌
```

---

### ✅ Correct Version

```java id="cs7"
if(age == 18) { }
```

---

## 🔥 3. Contrast & Decision Layer

| Situation             | Best Choice |
| --------------------- | ----------- |
| Range conditions      | `if-else`   |
| Multiple fixed values | `switch`    |
| Complex logic         | `if-else`   |

👉 `switch` improves readability but is less flexible than `if-else`.

---

## 📏 4. Rules & Constraints

- Condition must return `boolean`
- `=` is assignment, `==` is comparison
- `switch` supports:
  - `int`, `char`, `String`, `enum`

- `break` prevents fall-through in `switch`

---

## 💥 5. Error Handling and Common Bugs

### ❗ Logical Error (Assignment in Condition)

```java id="cs8"
boolean flag = false;

if(flag = true) { // ❌ always true
    System.out.println("Runs always");
}
```

---

### ❗ Fall-through in `switch`

```java id="cs9"
switch(day) {
    case 1: System.out.println("Mon");
    case 2: System.out.println("Tue");
}
```

👉 Missing `break` → both execute

---

## ⚙️ 6. Under the Hood (When Needed)

- `if` → compiled into **conditional jump instructions**
- JVM evaluates condition → jumps to appropriate block

👉 No magic, just branching logic.

---

## 🧩 7. Practical Applications

- Login validation systems
- Role-based access (Admin/User)
- Feature toggles
- Decision-making in business logic

---

## ❌ 8. Misuse Cases

### ❌ Deep Nesting (Unreadable Code)

```java id="cs10"
if(user != null){
    if(user.isActive()){
        if(user.isAdmin()){
            System.out.println("Access granted");
        }
    }
}
```

---

### ✅ Refactored Version (Better Approach)

```java id="cs11"
if(user == null) return;
if(!user.isActive()) return;
if(!user.isAdmin()) return;

System.out.println("Access granted");
```

👉 Improves readability and maintainability.

---

## 🧠 9. Concept Stress Test

- What if conditions grow to 10+?
  → Code becomes unreadable

- What if logic changes frequently?
  → Hardcoded conditions fail

👉 Solution:

- Use design patterns (Strategy, Polymorphism) later

---

## 🎯 Key Takeaways

- Control statements enable decision-making
- Choose between `if-else` and `switch` wisely
- Avoid deep nesting → use cleaner logic
- Always test edge cases and conditions

---
