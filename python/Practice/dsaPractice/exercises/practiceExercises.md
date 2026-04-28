# 📘 Python Practice Exercises: Concept-Based Progression

Welcome! These exercises are designed to systematically build Python proficiency. Each section targets a core programming concept, provides detailed problem statements, and includes reasoning guides to help you develop clean, efficient, and academically sound code.

> 💡 **Usage Tip:** Create a separate `.py` file for each exercise. Use `pytest` or built-in `assert` statements to verify your solutions before moving on.

---

## 📌 Section 1: Variables, Data Types, and Basic Operations

### Exercise 1.1: Precision Temperature Converter
**Objective:** Build a robust temperature conversion script.
**Requirements:**
- Prompt the user for a numeric temperature value and a unit (`C` or `F`)
- Validate input: reject values below absolute zero (`< -273.15°C` or `< -459.67°F`)
- Convert using standard formulas:  
  `F = (C × 9/5) + 32`  
  `C = (F − 32) × 5/9`
- Output the result formatted to exactly 2 decimal places

**Expected I/O:**
```
Enter temperature value: 36.6
Enter unit (C/F): C
Converted temperature: 97.88°F
```

### Exercise 1.2: String Parser & Formatter
**Objective:** Manipulate and standardize user input strings.
**Requirements:**
- Accept a full name string (e.g., `"  dr. john A. smith  "`)
- Strip leading/trailing whitespace
- Split into first, middle (if present), and last components
- Output format: `"Smith, John A."` (Title-cased, last name first, comma-separated)
- Handle missing middle names gracefully without raising index errors

**Critical Thinking Prompt:**  
How does Python's string immutability affect how you manipulate and reassign string data? Why must `strip()` be applied before `split()` in this workflow?

#### 🔍 Syntax & Logic Guide
- **Type Casting & Validation:** Wrap `float()` in `try/except ValueError` to catch non-numeric input.
- **String Methods:** `.strip()`, `.split()`, `.title()`, and conditional indexing.
- **F-Strings:** `f"{value:.2f}"` enforces fixed decimal precision.
- **Reasoning Steps:** Input → Clean → Validate Range/Type → Apply Formula → Format → Output.

---

## 📌 Section 2: Control Flow (Conditionals & Loops)

### Exercise 2.1: Academic Grade Classifier
**Objective:** Map numeric scores to letter grades with continuous user interaction.
**Requirements:**
- Accept numeric scores between 0–100
- Map to grades: A (90–100), B (80–89), C (70–79), D (60–69), F (<60)
- Return `"Invalid Score"` for out-of-range or non-numeric inputs
- Run inside a `while` loop until the user types `"quit"`

### Exercise 2.2: Optimized Prime Checker
**Objective:** Implement an efficient primality test.
**Requirements:**
- Write `is_prime(n)` returning `True`/`False`
- Handle edge cases: `n ≤ 1` (not prime), `2` (prime), even numbers (>2, not prime)
- Loop only up to `int(n**0.5) + 1` to check for divisors
- Include a driver loop that tests and prints all primes from 1 to 50

**Critical Thinking Prompt:**  
Why does checking divisors only up to `√n` reduce time complexity from O(n) to O(√n)? How would you adapt this algorithm for cryptographic-grade large integers?

#### 🔍 Syntax & Logic Guide
- **Conditionals:** `if/elif/else` chains with clear boundary checks.
- **Loops:** `while` for interactive sessions; `for i in range(2, limit):` for iteration.
- **Optimization Logic:** If `n = a × b`, at least one factor must be ≤ √n. Checking beyond √n is mathematically redundant.
- **Control Keywords:** `break` exits early on first divisor found; `continue` skips unnecessary iterations.

---

## 📌 Section 3: Functions and Scope

### Exercise 3.1: Flexible Palindrome Validator
**Objective:** Create a configurable string validation function.
**Requirements:**
- Define `is_palindrome(text: str, ignore_case: bool = True, ignore_punctuation: bool = True) -> bool`
- Strip punctuation and normalize case based on boolean flags
- Return `True` if cleaned string reads identically forward and backward
- Include a comprehensive docstring and type hints

### Exercise 3.2: Dynamic Argument Aggregator
**Objective:** Master flexible function signatures.
**Requirements:**
- Define `aggregate_stats(*args: float, operation: str = "sum", **kwargs) -> float`
- Support operations: `"sum"`, `"mean"`, `"max"`, `"min"`
- Use `**kwargs` to handle optional flags like `ignore_zeros: bool = True`
- Raise `ValueError` for unsupported operations or empty positional arguments

**Critical Thinking Prompt:**  
When is `*args`/`**kwargs` preferable over fixed parameters? How does Python's LEGB (Local, Enclosing, Global, Built-in) scope resolution affect variable access in nested functions?

#### 🔍 Syntax & Logic Guide
- **Function Signature:** `def name(param: type = default) -> return_type:`
- **Scope Rules:** Variables inside functions are local by default. `global`/`nonlocal` modify this behavior but should be used sparingly.
- **Argument Unpacking:** `*args` → tuple of positional args; `**kwargs` → dict of keyword args.
- **Reasoning Steps:** Validate inputs → Apply transformation logic → Compute result → Return with proper type.

---

## 📌 Section 4: Data Structures (Lists, Dictionaries, Sets, Tuples)

### Exercise 4.1: Word Frequency Analyzer
**Objective:** Process text and count word occurrences.
**Requirements:**
- Accept a paragraph string
- Convert to lowercase, remove punctuation, split into words
- Count frequencies using a dictionary
- Output words sorted by frequency (descending), then alphabetically for ties

### Exercise 4.2: Set-Based Data Filter
**Objective:** Leverage set theory for efficient list operations.
**Requirements:**
Given:
```python
list_a = [1, 2, 2, 3, 4, 5]
list_b = [4, 5, 5, 6, 7, 8]
```
- Convert to sets to remove duplicates
- Compute intersection (`&`) and symmetric difference (`^`)
- Return results as sorted lists without duplicates

**Critical Thinking Prompt:**  
Why is dictionary/set lookup O(1) on average compared to list lookup O(n)? When would you prefer a `tuple` over a `list` for data integrity?

#### 🔍 Syntax & Logic Guide
- **Dict/Sorting:** `sorted(freq_dict.items(), key=lambda x: (-x[1], x[0]))`
- **Set Operations:** `set_a & set_b` (intersection), `set_a ^ set_b` (symmetric difference)
- **Performance Note:** Hash-based structures use open addressing or chaining for collisions. Worst-case degrades to O(n), but average remains O(1).
- **Reasoning Steps:** Clean data → Hash/Count → Sort/Filter → Format output.

---

## 📌 Section 5: File I/O and Exception Handling

### Exercise 5.1: Structured Log Parser
**Objective:** Safely read, parse, and summarize external data.
**Requirements:**
- Read `access.log` (format: `TIMESTAMP IP STATUS_CODE MESSAGE`)
- Count HTTP status code occurrences
- Write summary to `summary.txt` as `STATUS_CODE: COUNT`
- Use `with open(...)` for deterministic resource management
- Handle `FileNotFoundError` and malformed lines gracefully

### Exercise 5.2: Safe Data Backup Utility
**Objective:** Implement robust file operations with error recovery.
**Requirements:**
- Define `backup_data(source_path: str, dest_path: str) -> bool`
- Verify source is readable and destination is writable
- Use `try/except/else/finally` to manage execution flow and cleanup
- Log success/failure and return boolean status

**Critical Thinking Prompt:**  
Why is the `with` statement preferred over manual `file.close()`? What happens to OS file buffers and memory if an exception occurs before explicit closure?

#### 🔍 Syntax & Logic Guide
- **Context Managers:** `with open(...) as f:` calls `__enter__()` and guarantees `__exit__()` even on exceptions.
- **Exception Blocks:** 
  - `try`: risky operations
  - `except`: catch/handle errors
  - `else`: runs only if no exception occurred
  - `finally`: always executes (cleanup, logging, resource release)
- **File Modes:** `"r"`, `"w"`, `"a"`, `"rb"`, `"wb"`
- **Reasoning Steps:** Validate paths → Open safely → Read/Process → Write → Handle errors → Ensure cleanup.

---

## 📌 Section 6: Object-Oriented Programming (OOP)

### Exercise 6.1: Bank Account Manager
**Objective:** Design a secure, encapsulated class.
**Requirements:**
- Class `BankAccount` with private attributes: `__owner`, `__balance`
- Methods: `deposit(amount)`, `withdraw(amount)`, `get_balance()`
- Validation: Reject negative amounts, prevent overdrafts
- Implement `__str__` returning `"Account: {owner} | Balance: ${balance:.2f}"`

### Exercise 6.2: Inheritance & Method Overriding
**Objective:** Model hierarchical relationships with polymorphism.
**Requirements:**
- Base class `Employee(name: str, salary: float)` with `calculate_bonus() -> float`
- `Manager` subclass: bonus = `salary * 0.15`
- `Developer` subclass: bonus = `salary * 0.10 + (project_count * 500)`
- Use `super().__init__()` and maintain type hints throughout

**Critical Thinking Prompt:**  
When should you prefer composition (`self.account = BankAccount(...)`) over inheritance? How does Python's name mangling (`__attr`) differ from convention-based protection (`_attr`)?

#### 🔍 Syntax & Logic Guide
- **Class Structure:** 
  ```python
  class ClassName:
      def __init__(self, param: type) -> None:
          self.attr = param
  ```
- **Encapsulation:** `__attr` triggers `_ClassName__attr` mangling to prevent accidental external modification.
- **Inheritance:** `class Child(Parent):` inherits attributes/methods; `super()` delegates to parent constructor.
- **Dunder Methods:** `__str__` (user-facing), `__repr__` (developer-facing), `__init__` (initializer).
- **Reasoning Steps:** Define state → Enforce invariants → Implement behavior → Extend via inheritance → Document interfaces.

---

## 🧠 How to Approach These Exercises (Reasoning Steps)

1. **Decompose:** Identify inputs, constraints, transformations, and expected outputs.
2. **Pseudocode First:** Draft plain-English logic before writing syntax.
3. **Implement Incrementally:** Build and test one function/block at a time.
4. **Edge Cases:** Test boundaries (empty inputs, zeros, negatives, max values, type mismatches).
5. **Refactor:** Replace repetition with functions, add type hints, enforce PEP 8 styling, and document thoroughly.

---

## 📚 Academic Integrity & Citation Guidance

✅ **Academic Integrity Reminder:**  
These exercises are intended for personal skill development and coursework practice. When submitting work in academic settings:
- Write all code independently unless collaboration is explicitly permitted.
- Do not submit AI-generated code without proper attribution or institutional approval.
- Cite all external references, documentation, or third-party libraries used.

📖 **Suggested Citations (APA 7th Edition):**
- Python Software Foundation. (n.d.). *Python 3 documentation*. Retrieved April 2026, from https://docs.python.org/3/
- Sweigart, A. (2019). *Automate the boring stuff with Python: Practical programming for total beginners* (2nd ed.). No Starch Press.
- Lutz, M. (2013). *Learning Python* (5th ed.). O'Reilly Media.

📝 **MLA Format Alternative:**
Python Software Foundation. *Python 3 Documentation*. https://docs.python.org/3/. Accessed 24 Apr. 2026.

---

## 🛠 Next Steps & Self-Assessment
- Run `python -m pytest` or write simple `assert` blocks to validate outputs.
- Track your completion rate and note which concepts require additional review.
- For advanced practice, refactor these solutions using `dataclasses`, `typing.Protocol`, or `pydantic` for validation.
- Would you like companion unit test templates, Jupyter Notebook scaffolding, or a transition to data science libraries (NumPy/Pandas/Polars)?

*Happy coding & rigorous problem solving!* 🐍✨