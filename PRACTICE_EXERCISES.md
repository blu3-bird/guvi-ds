# 📚 Comprehensive Practice Exercises - Data Science Python Revision

Based on your repository, I've created practice exercises covering **all the concepts** you've learned. These are organized by topic for effective revision.

---

## 📋 Topics Covered in Your Repo

1. **Python Basics**: f-strings, string functions, data types
2. **Data Structures**: Lists, Sets, Tuples, Dictionaries
3. **Control Flow**: Conditional statements (if/else), For loops, While loops
4. **Functions**: Creating and using functions
5. **Input/Output**: input() function, type casting
6. **Problem Solving**: Codekata problems (easy & medium)
7. **Data Science Concepts**: SQL, Data Preprocessing, Visualization, Regression models

---

## 🔥 Practice Exercises

### **Section 1: Python String Operations**

#### Exercise 1.1: F-String Mastery
```python
# Practice creating formatted strings with:
# 1. Variables and literals combined
# 2. Mathematical expressions
# 3. Function calls inside f-strings
# 4. Multi-line f-strings

# Task: Create a student report card formatter
student_name = "John Doe"
marks = [85, 90, 78, 92, 88]
average = sum(marks) / len(micks)

# Expected output format:
# Student: John Doe
# Marks: [85, 90, 78, 92, 88]
# Average: 86.6
# Grade: A
```

#### Exercise 1.2: String Methods Challenge
```python
# Given a messy text input, clean it using string methods:
text = "   PyThOn DaTa ScIeNcE   "

# Tasks:
# 1. Convert to lowercase
# 2. Convert to title case
# 3. Remove leading/trailing spaces
# 4. Check if it contains only alphabets
# 5. Replace spaces with hyphens
```

#### Exercise 1.3: String Analysis
```python
# Write a program that:
# 1. Counts vowels and consonants in a string
# 2. Finds the first occurrence of each character
# 3. Checks if two strings are anagrams
# 4. Reverses a string without slicing
```

---

### **Section 2: Data Structures**

#### Exercise 2.1: List Operations
```python
# Create a shopping list manager:
shopping_list = ['apple', 'banana', 'milk']

# Implement:
# 1. Add item (append)
# 2. Add multiple items (extend)
# 3. Insert at specific position
# 4. Remove first occurrence of an item
# 5. Remove last item (pop)
# 6. Slice to get first 3 items
# 7. Sort alphabetically
# 8. Find index of an item
```

#### Exercise 2.2: Set Operations
```python
# Given two sets of student IDs:
class_a = {101, 102, 103, 104, 105}
class_b = {103, 104, 106, 107, 108}

# Find:
# 1. Students in both classes (intersection)
# 2. All unique students (union)
# 3. Students only in class_a (difference)
# 4. Students in either class but not both (symmetric difference)
# 5. Add a new student to class_a
# 6. Remove a student from class_b
```

#### Exercise 2.3: Dictionary Practice
```python
# Create a student database:
student_db = {
    'name': 'Alice',
    'age': 20,
    'courses': ['Math', 'Science'],
    'grades': {'Math': 90, 'Science': 85}
}

# Tasks:
# 1. Add a new key-value pair (email)
# 2. Update age
# 3. Access nested dictionary value
# 4. Add a new course and grade
# 5. Delete a key
# 6. Get all keys, values, and items
```

#### Exercise 2.4: Tuple Immutability
```python
# Create coordinates as tuples:
point_2d = (5, 10)
point_3d = (3, 7, 12)

# Tasks:
# 1. Access individual elements
# 2. Try to modify (observe error)
# 3. Unpack tuple into variables
# 4. Convert tuple to list, modify, convert back
# 5. Find length of tuple
```

---

### **Section 3: Control Flow - Conditionals**

#### Exercise 3.1: Number Classifier
```python
# Write a program that classifies a number as:
# 1. Positive, Negative, or Zero
# 2. Even or Odd
# 3. Prime or Composite
# 4. Perfect Square or Not
# 5. Armstrong Number or Not (e.g., 153 = 1³ + 5³ + 3³)
```

#### Exercise 3.2: Grade Calculator
```python
# Enhanced grading system:
# 90-100: A+ (Excellent)
# 80-89: A (Very Good)
# 70-79: B (Good)
# 60-69: C (Average)
# 50-59: D (Pass)
# Below 50: Fail

# Also calculate:
# - GPA (Grade Point Average)
# - Class rank based on percentage
```

#### Exercise 3.3: Leap Year Validator
```python
# Complete leap year logic:
# Divisible by 4 AND (not divisible by 100 OR divisible by 400)
# Test with years: 1900, 2000, 2024, 2100
```

#### Exercise 3.4: Range Checker
```python
# Given 3 numbers N, L, R:
# Check if N is between L and R (inclusive)
# Extend: Check if N is exactly in the middle of L and R
```

---

### **Section 4: Loops (For & While)**

#### Exercise 4.1: Pattern Printing
```python
# Print these patterns using loops:
# 1. Right triangle of stars
# 2. Pyramid pattern
# 3. Number triangle (1, 12, 123, 1234)
# 4. Floyd's triangle
```

#### Exercise 4.2: Summation Problems
```python
# Calculate:
# 1. Sum of first N natural numbers
# 2. Sum of squares of first N numbers
# 3. Sum of cubes of first N numbers
# 4. Sum of even numbers up to N
# 5. Sum of odd numbers up to N
# 6. Harmonic series: 1 + 1/2 + 1/3 + ... + 1/N
```

#### Exercise 4.3: Factorial & Fibonacci
```python
# Using while loop:
# 1. Find factorial of N
# 2. Generate Fibonacci sequence up to N terms
# 3. Find Nth Fibonacci number
```

#### Exercise 4.4: Number Manipulation
```python
# Given a number:
# 1. Reverse the digits
# 2. Check if palindrome
# 3. Count digits
# 4. Sum of digits
# 5. Product of digits
# 6. Find next power of 2
```

#### Exercise 4.5: Array/List Processing
```python
# Given an array of numbers:
# 1. Find maximum and minimum
# 2. Find second largest element
# 3. Count occurrences of each element
# 4. Find elements repeated K times
# 5. Check if array is sorted
# 6. Rotate array by K positions
```

---

### **Section 5: Functions**

#### Exercise 5.1: Utility Functions
```python
# Create reusable functions:
def is_prime(n):
    """Check if a number is prime"""
    pass

def gcd(a, b):
    """Find GCD of two numbers"""
    pass

def lcm(a, b):
    """Find LCM of two numbers"""
    pass

def is_palindrome(s):
    """Check if string is palindrome"""
    pass

def count_vowels(s):
    """Count vowels in a string"""
    pass
```

#### Exercise 5.2: Math Functions
```python
# Implement without using built-in functions:
def power(base, exp):
    """Calculate base^exp"""
    pass

def sqrt_approx(n):
    """Approximate square root using binary search"""
    pass

def factorial(n):
    """Calculate factorial recursively and iteratively"""
    pass
```

#### Exercise 5.3: List Functions
```python
# Create functions that work with lists:
def find_max(lst):
    """Return maximum element"""
    pass

def find_min(lst):
    """Return minimum element"""
    pass

def reverse_list(lst):
    """Return reversed list"""
    pass

def remove_duplicates(lst):
    """Remove duplicates preserving order"""
    pass

def merge_sorted_lists(list1, list2):
    """Merge two sorted lists"""
    pass
```

---

### **Section 6: Input/Output & Type Casting**

#### Exercise 6.1: Interactive Programs
```python
# Create programs that:
# 1. Take user input until they enter 'exit'
# 2. Validate input (ensure it's a number)
# 3. Handle invalid inputs gracefully
# 4. Convert string input to appropriate data types
```

#### Exercise 6.2: Data Conversion
```python
# Practice type casting:
# 1. String to int, float
# 2. Int to string, float
# 3. Float to int, string
# 4. List to tuple, set
# 5. Tuple to list
# 6. Set to list
```

---

### **Section 7: Codekata-Style Problems**

#### Easy Level Problems

```python
# Problem 1: Product of Digits
# Given N, print product of its digits
# Input: 2143 → Output: 24

# Problem 2: String Middle Modification
# Replace middle character(s) with '*'
# Input: "hello" → Output: "he*lo"
# Input: "test" → Output: "te**"

# Problem 3: Composite Number Check
# Print 'yes' if composite, else 'no'

# Problem 4: Factors of a Number
# Print all factors of N

# Problem 5: Perfect Square Product
# Given N, M check if N*M is perfect square

# Problem 6: Vowel Counter
# Count vowels in a string (case-insensitive)

# Problem 7: String Length Without len()
# Find length without using len() function

# Problem 8: Case-Sensitive Equality
# Compare two strings case-sensitively

# Problem 9: Common Characters
# Check if two strings share any character

# Problem 10: Round to Nearest Greater Integer
# Input: 2.6 → Output: 3
```

#### Medium Level Problems

```python
# Problem 1: Kth Smallest Element
# Find Kth smallest, return -1 if doesn't exist

# Problem 2: Second Smallest Element
# Handle duplicates properly

# Problem 3: First Occurrence Position
# Find position of character (1-indexed)

# Problem 4: Count String Occurrences
# Count how many times substring appears

# Problem 5: Pair Sum Check
# Check if any two elements sum to X

# Problem 6: Minimum Odd Quotient Factor
# Find factor that gives odd quotient

# Problem 7: Common Elements in Sorted Arrays
# Print common elements in sorted order

# Problem 8: Elements Less Than K (Sorted)
# Print elements < K in sorted order

# Problem 9: Descending Order Below N
# Print elements < N in descending order

# Problem 10: Numbers Repeated K Times
# Find numbers appearing exactly K times

# Problem 11: Difference Check
# Check if any two numbers differ by K

# Problem 12: Missing Number
# Find missing number from 1 to N

# Problem 13: Unique Elements
# Print elements appearing exactly once

# Problem 14: Pair Sum Count
# Count pairs that sum to X
```

---

### **Section 8: Data Science Fundamentals**

#### Exercise 8.1: Data Preprocessing Practice
```python
# Simulate data preprocessing tasks:
data = [12, 15, 18, None, 22, None, 28, 30]

# Tasks:
# 1. Handle missing values (replace with mean)
# 2. Normalize data (min-max scaling)
# 3. Standardize data (z-score normalization)
# 4. Remove outliers (beyond 2 standard deviations)
```

#### Exercise 8.2: Basic Statistics
```python
# Calculate without libraries:
numbers = [23, 45, 67, 89, 12, 34, 56, 78, 90, 11]

# Find:
# 1. Mean
# 2. Median
# 3. Mode
# 4. Range
# 5. Variance
# 6. Standard Deviation
```

#### Exercise 8.3: Percentage Calculations
```python
# Like your class5 module:
scores = [12, 14, 20, 9, 5, 18, 9]
max_score = 20

# Calculate percentage for each score
# Store in new list
# Find average percentage
# Categorize into grades
```

---

### **Section 9: Advanced Problem Solving**

#### Exercise 9.1: Combined Concepts
```python
# Problem: Student Performance Analyzer
# Input: Multiple students with marks in different subjects
# Output:
# - Average marks per student
# - Top performer
# - Subject-wise topper
# - Grade distribution
# - Pass/Fail count
```

#### Exercise 9.2: Real-world Scenarios
```python
# Scenario 1: E-commerce Cart
# - Add/remove items
# - Apply discounts
# - Calculate total with tax
# - Find most expensive item

# Scenario 2: Bank Account System
# - Deposit/withdraw
# - Check balance
# - Transaction history
# - Interest calculation

# Scenario 3: Library Management
# - Issue/return books
# - Track due dates
# - Fine calculation
# - Book availability
```

---

## 🎯 Challenge Projects

### Project 1: Number Theory Toolkit
Create a complete toolkit with functions for:
- Prime checking, factorization
- GCD, LCM calculations
- Armstrong numbers, perfect numbers
- Fibonacci generator
- Palindrome checker

### Project 2: Text Analyzer
Build a program that analyzes text:
- Word count, character count
- Vowel/consonant ratio
- Most frequent words
- Sentence analysis
- Readability score

### Project 3: Data Statistics Calculator
Implement statistical operations:
- Mean, median, mode
- Variance, standard deviation
- Percentiles
- Correlation coefficient
- Data visualization (basic ASCII charts)

### Project 4: Quiz Application
Create an interactive quiz:
- Multiple choice questions
- Score tracking
- Timer (optional)
- Result analysis
- Difficulty levels

---

## 📝 Self-Assessment Checklist

After practicing, check if you can:

- [ ] Use f-strings confidently for formatting
- [ ] Apply all string methods appropriately
- [ ] Choose correct data structure for a problem
- [ ] Write nested loops for complex patterns
- [ ] Create reusable functions with proper parameters
- [ ] Handle user input with validation
- [ ] Solve Codekata easy problems independently
- [ ] Approach medium problems systematically
- [ ] Explain time complexity of your solutions
- [ ] Debug errors effectively

---

## 💡 Tips for Effective Practice

1. **Start Simple**: Begin with easy problems, gradually increase difficulty
2. **Understand First**: Don't just copy code; understand the logic
3. **Multiple Solutions**: Try solving same problem differently
4. **Time Yourself**: Practice coding under time pressure
5. **Review Regularly**: Revisit old problems after a week
6. **Document**: Comment your code explaining the approach
7. **Test Thoroughly**: Create test cases including edge cases

---

## 🔗 Next Steps

After mastering these basics:
1. Learn NumPy for numerical computing
2. Study Pandas for data manipulation
3. Explore Matplotlib/Seaborn for visualization
4. Dive into Scikit-learn for ML algorithms
5. Practice SQL queries extensively
6. Work on real datasets from Kaggle

---

**Happy Practicing! 🚀**

Remember: Consistency is key. Practice daily, even if it's just one problem!
