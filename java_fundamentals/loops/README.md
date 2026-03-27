# 🔁 Loops

## 🧠 1. Why + Definition

### ❓ Problem

Without loops:

- You repeat the same code multiple times
- Code becomes unmaintainable and error-prone
- Impossible to handle large datasets (e.g., 1M records)

👉 Loops allow **controlled repetition**.

---

### 📌 Definition

A loop is used to execute a block of code repeatedly until a condition is met.

---

### 🌍 Real-world Analogy

Think of checking attendance:

- Instead of calling each student manually, you iterate through a list.

---

## 💻 2. Syntax and Implementation

### ✅ `for` Loop (Known iterations)

```java
for(int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

---

### ✅ `while` Loop (Unknown iterations)

```java
int i = 0;
while(i < 5) {
    System.out.println(i);
    i++;
}
```

---

### ✅ `do-while` Loop (Runs at least once)

```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while(i < 5);
```

---

### ✅ Enhanced `for-each` Loop (Read-only traversal)

```java
int[] arr = {1, 2, 3, 4};

for(int num : arr) {
    System.out.println(num);
}
```

---

### ⚠️ Wrong Implementation (Common Mistakes)

#### ❌ Infinite Loop

```java
int i = 0;
while(i < 5) {
    System.out.println(i);
    // Missing i++ → infinite loop
}
```

---

#### ❌ Off-by-One Error

```java
int[] arr = new int[5];

for(int i = 0; i <= arr.length; i++) { // ❌
    System.out.println(arr[i]);
}
```

---

### ✅ Correct Version

```java
for(int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

---

## 🔥 3. Contrast & Decision Layer

| Situation                                 | Best Choice  |
| ----------------------------------------- | ------------ |
| Known number of iterations                | `for` loop   |
| Condition-based execution                 | `while` loop |
| Execute at least once                     | `do-while`   |
| Traversing arrays/collections (read-only) | `for-each`   |

👉 Choosing the right loop improves readability and reduces bugs.

---

## 📏 4. Rules & Constraints

- Loop condition must evaluate to `boolean`
- Missing update statement → infinite loop
- `for-each` cannot modify array indices
- Be careful with loop boundaries (`<` vs `<=`)

---

## 💥 5. Error Handling and Common Bugs

### ❗ Infinite Loop

Cause: Missing update condition
Effect: Program hangs / CPU usage spikes

---

### ❗ Array Index Error

```java
arr[arr.length] // ❌ out of bounds
```

Exception:

```
ArrayIndexOutOfBoundsException
```

---

### ❗ Modifying Collection During Iteration

(Advanced case)

```java
for(String s : list) {
    list.remove(s); // ❌
}
```

---

## ⚙️ 6. Under the Hood (When Needed)

- Loops are compiled into **jump instructions**
- JVM repeatedly checks condition → executes block
- Time complexity depends on number of iterations

---

## 📊 7. Performance Consideration

### ⏱ Single Loop

```java
for(int i=0;i<n;i++)
```

👉 Time Complexity: O(n)

---

### ⚠️ Nested Loop

```java
for(int i=0;i<n;i++){
    for(int j=0;j<n;j++){
```

👉 Time Complexity: O(n²)

---

👉 Poor loop design = performance bottleneck

---

## 🧩 8. Practical Applications

- Iterating database records
- Searching elements
- Processing arrays or lists
- Reading files line by line

---

## ❌ 9. Misuse Cases

### ❌ Unnecessary Nested Loops

Leads to:

- Slow performance
- Complex debugging

---

### ❌ Using Loop Instead of Built-in Methods

Later concepts (Streams, Collections) provide better alternatives.

---

## 🧠 10. Concept Stress Test

- What happens if loop runs 10 million times?
- Can it be optimized?
- Can it be parallelized?

👉 Loops don’t scale well without optimization.

---

## 🎯 Key Takeaways

- Loops = repetition with control
- Always choose the right loop type
- Watch for infinite loops and boundary errors
- Think about performance early

---
