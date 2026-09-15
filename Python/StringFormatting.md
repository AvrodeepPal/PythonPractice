Great question 👌 — **string formatting** is super important in Python because it lets you **insert variables or values into strings** in a clean and controlled way.

Python has **4 main styles** of string formatting (from old → modern). Let’s go step by step with examples.

---

# 🔹 1. **Old Style (`%` formatting)**

Similar to C’s `printf`.

```python
name = "Alice"
age = 25

print("Hello, %s. You are %d years old." % (name, age))
```

Output:

```
Hello, Alice. You are 25 years old.
```

* `%s` → string
* `%d` → integer
* `%f` → float

⚠️ Considered **outdated**, but still works.

---

# 🔹 2. **`str.format()` Method**

Introduced in Python 2.6/3.0.

```python
name = "Bob"
age = 30
print("Hello, {}. You are {} years old.".format(name, age))
```

Output:

```
Hello, Bob. You are 30 years old.
```

👉 You can also specify positions:

```python
print("Hello, {0}. Next year you’ll be {1}.".format(name, age+1))
```

👉 Or use named placeholders:

```python
print("Hello, {name}. You are {age} years old.".format(name="Charlie", age=28))
```

---

# 🔹 3. **F-Strings (Python 3.6+) ✅ Most popular**

Fast, clean, and modern.

```python
name = "David"
age = 35
print(f"Hello, {name}. You are {age} years old.")
```

Output:

```
Hello, David. You are 35 years old.
```

👉 You can even put expressions inside:

```python
print(f"In 5 years, {name} will be {age + 5}.")
```

👉 Formatting numbers:

```python
pi = 3.1415926535
print(f"Pi rounded to 2 decimals: {pi:.2f}")
print(f"Pi as percentage: {pi:.2%}")
```

Output:

```
Pi rounded to 2 decimals: 3.14
Pi as percentage: 314.16%
```

---

# 🔹 4. **Template Strings (from `string` module)**

Good for cases where you want **safe substitution** (e.g., user-provided data).

```python
from string import Template

t = Template("Hello, $name. You are $age years old.")
print(t.substitute(name="Eve", age=40))
```

Output:

```
Hello, Eve. You are 40 years old.
```

---

# 🔹 Quick Comparison

| Method         | Example                                | Modern use?          |
| -------------- | -------------------------------------- | -------------------- |
| `%` formatting | `"Hi %s" % name`                       | ❌ Old, rarely used   |
| `.format()`    | `"Hi {}".format(name)`                 | ⚠️ Still okay        |
| f-strings      | `f"Hi {name}"`                         | ✅ Best, fastest      |
| `Template`     | `Template("Hi $name").substitute(...)` | ✅ When safety needed |

---

✅ **Summary**:

* Use **f-strings** (`f"{var}"`) in modern Python (cleanest + fastest).
* Use `.format()` if you need advanced formatting in older Python.
* Use `Template` when formatting **user inputs safely**.

---

Would you like me to also show you a **table of number/date formatting options** (like padding, alignment, percentages, dates) so you have a quick reference?

