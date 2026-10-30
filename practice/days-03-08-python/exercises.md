# Practice: Python, Days 3 to 8

One section per day. Save your solutions in `my-progress/` as `day03.py`, `day04.py` and so on. Try each exercise for about 10 minutes before looking anything up. Where an expected output is shown, yours should match.

Run a file with `python day03.py`, or paste the code into a Colab cell.

---

## Day 3: Syntax, variables and data types

1. Store your name, department and year in three variables. Print one sentence using an f-string, for example: `Aarav is in year 2 of CSE.`
2. Swap the values of two variables `a = 5` and `b = 9` without using a third variable.
3. Use `type()` on each of these and print the result: `42`, `3.14`, `"42"`, `True`, `None`.
4. Convert `"42"` to an integer, `3.9` to an integer, and `0`, `1`, `""` and `"a"` to booleans. Print each result. Write one line explaining what `int(3.9)` does to the decimal part.
5. Ask for a temperature in Celsius with `input()` and print it in Fahrenheit.
6. Ask for weight in kg and height in metres. Print the BMI rounded to 1 decimal place.
7. Convert 4000 seconds to hours, minutes and seconds using `//` and `%`. Expected: `1 hours 6 minutes 40 seconds`.
8. Take the string `"  Machine Learning  "`. Remove the outer spaces, convert to upper case, replace `"LEARNING"` with `"INTELLIGENCE"`, count how many times `"N"` appears, and print the first 7 characters.
9. Write a simple interest calculator: principal, rate and years from the user, print the interest.

Check: what does `7 / 2` give? What does `7 // 2` give? What does `-7 // 2` give? Run it and see if you predicted correctly.

---

## Day 4: Lists, tuples, sets and dictionaries

1. Given `marks = [72, 85, 90, 64, 85, 78]`, print the maximum, minimum, sum and average. Print the list sorted in descending order. Print it again with duplicates removed.
2. With the same list, print the first three items, the last two items, every second item, and the list reversed. Use slicing for all four.
3. Use a list comprehension to build the squares of the even numbers from 1 to 20. Expected: `[4, 16, 36, 64, 100, 144, 196, 256, 324, 400]`.
4. Store a point as a tuple `(3, 4)`. Unpack it into `x` and `y` and print its distance from the origin. Expected: `5.0`.
5. Two clubs have members `["Asha", "Ravi", "Kiran", "Sana"]` and `["Ravi", "Sana", "Tej", "Uma"]`. Using sets, print members in both, in either, and only in the first.
6. Count the frequency of each word in `"to be or not to be that is the question"` using a dictionary. Expected: `to` and `be` appear 2 times each.
7. Build a dictionary of students with a name for each key and a dictionary of marks as the value, for at least four students. Print the name of the student with the highest total.
8. Given the 3 by 3 matrix `[[1, 2, 3], [4, 5, 6], [7, 8, 9]]` stored as a list of lists, build its transpose without NumPy. Expected: `[[1, 4, 7], [2, 5, 8], [3, 6, 9]]`.

Check: which of these can be a dictionary key, and which cannot: a list, a tuple, a string, a set? Try each and read the error.

---

## Day 5: Loops and conditionals

1. FizzBuzz for 1 to 50. Print `Fizz` for multiples of 3, `Buzz` for multiples of 5, `FizzBuzz` for both, the number otherwise.
2. Write a leap year check. A year is a leap year if it is divisible by 4, except years divisible by 100 unless also divisible by 400. Test 1900, 2000, 2024, 2100.
3. Sum the digits of a number entered by the user. Use a loop and no string conversion. Expected: 4821 gives 15.
4. Write a prime check. Then print every prime below 100. There are 25 of them.
5. Grade classifier: marks 90 and above A, 75 to 89 B, 60 to 74 C, 40 to 59 D, below 40 F. Use `if`, `elif` and `else`.
6. Print a multiplication table for 1 to 10 using nested loops. Then print a right triangle of stars with 5 rows.
7. Set a secret number in your code. Use a `while` loop to keep asking for guesses and tell the user higher or lower until correct.
8. Print the first 15 Fibonacci numbers. Expected: `0 1 1 2 3 5 8 13 21 34 55 89 144 233 377`.
9. The Collatz rule: if n is even, halve it; if odd, take 3n + 1. Count steps until n reaches 1 starting from 27. Expected: 111 steps.

Check: what does `break` do in a loop, and what does `continue` do? Write a 5-line example of each.

---

## Day 6: Functions and built-ins

1. Write `mean(values)`, `median(values)` and `mode(values)` without importing `statistics`. Test with `[3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]`. The mean is about 3.91, the median is 4, the mode is 5.
2. Write `greet(name, greeting="Hello")`. Call it with and without the second argument, and with keyword arguments in a different order.
3. Write `sum_all(*args)` that adds any number of arguments, and `show_info(**kwargs)` that prints each key and value.
4. Write `factorial(n)` recursively. Then write `fib(n)` recursively and time it for n = 30. Then write an iterative version and compare the times.
5. Given `pairs = [("a", 3), ("b", 1), ("c", 2)]`, sort by the second item using `sorted` and a `lambda`.
6. For each of `map`, `filter`, `zip`, `enumerate`, `any` and `all`, write one example of your own and print the result.
7. Write `is_palindrome(text)` that ignores case, spaces and punctuation. Test with `"A man, a plan, a canal: Panama"`.
8. Add a docstring to each function you wrote today. Then write five `assert` statements that test `mean` and `is_palindrome`.
9. Write `safe_divide(a, b)` that returns `None` and prints a message when `b` is zero, using `try` and `except`. Write a second function that reads a file and handles `FileNotFoundError`.

Check: what is wrong with `def add(item, items=[])`? Call it three times and look at the result.

---

## Day 7: Object-oriented programming

1. Create a `Student` class with a name and a list of marks. Add a method `average()`. Make three students and print their averages.
2. Create a `BankAccount` class with `deposit` and `withdraw`. Raise an exception when a withdrawal exceeds the balance. Catch it where you call it.
3. Add `__str__` and `__repr__` to `Student`. Print a student and print a list of students, and notice the difference.
4. Write a base class `Shape` with an `area()` method that raises `NotImplementedError`. Create `Circle` and `Rectangle` that inherit from it and override `area()`. Put several shapes in a list and print the total area.
5. Add a class variable `count` to `Student` that increases each time a student is created. Print it after creating five students.
6. Give `Student` an `age` property that rejects values below 0 or above 120. Use `@property` and a setter.
7. Write a `Stack` class (push, pop, peek, is_empty) and a `Queue` class (enqueue, dequeue). Use each to solve one small problem: reversing a string with the stack, and processing tasks in order with the queue.
8. Challenge: a small library system with `Book` and `Member` classes. A member can borrow up to 3 books. Borrowing a book that is already out should fail with a clear message.

Check: what is the difference between a class variable and an instance variable? Write a short example that shows it.

---

## Day 8: Mini project, student grade manager

Build a command-line program that manages student marks. Put it in one file, `grade_manager.py`, or split it into a few modules.

Required features:

- Add a student by name.
- Add marks for a subject for a student.
- Show a student's average.
- Show the class average.
- Show the top student.
- Save all data to a JSON file and load it when the program starts.
- Show a menu in a loop until the user chooses to quit.

Requirements on how it is written:

- Use at least one class.
- Use functions or methods that each do one thing.
- Handle bad input without crashing (a non-number mark, a name that does not exist).
- Add a short README in the project folder that says how to run it.

Stretch goals, in any order:

- Letter grades with the thresholds from Day 5.
- Export a report to a text file.
- A rank list sorted by average.
- Basic tests with `assert`.

Review checklist before you commit:

- Does it run from a clean start with no saved file?
- Does it survive typing letters where a number is expected?
- Can someone else follow your code in 10 minutes?
- Did you remove leftover test prints?
