
# 🔍 Standalone Regex Tester & Complete Regular Expressions Guide

A professional, highly capable, dark-themed Regular Expression (Regex) tester built as a single, standalone `index.html` file. 

This project is specifically engineered to work offline on **restricted networks and intranets (such as Iran's National Internet / INTR)**. It requires zero external dependencies, no CDNs, and no API calls. 

Generated using prompt engineering with **Google Gemini**.

---

## 📑 Table of Contents

- [About the Tester App](#-about-the-tester-app)
  - [Features](#features)
  - [How to Use](#how-to-use)
  - [Screenshots](#screenshots)
- [The Complete Regex Guide](#-the-complete-regex-guide)
  - [What is a Regular Expression?](#what-is-a-regular-expression)
  - [JavaScript RegExp Flags](#javascript-regexp-flags)
  - [RegExp Group Modifiers](#regexp-group-modifiers)
  - [JavaScript Regex Flag Properties](#javascript-regex-flag-properties)
  - [Regular Expression Methods](#regular-expression-methods)
  - [RegExp Character Classes](#regexp-character-classes)
  - [RegExp Metacharacters](#regexp-metacharacters)
  - [RegExp Assertions (Anchors & Boundaries)](#regexp-assertions-anchors--boundaries)
  - [RegExp Quantifiers](#regexp-quantifiers)
  - [RegExp Groups](#regexp-groups)
- [Common Regex Patterns](#-common-regex-patterns)
- [Using Regex in Programming Languages](#-using-regex-in-programming-languages)
  - [JavaScript](#javascript)
  - [Python](#python)
  - [PHP](#php)
  - [Java](#java)
  - [C#](#c)
- [Author & Credits](#-author--credits)

---

## 💻 About the Tester App

### Features
- **$100\%$ Offline & Standalone:** No external CSS or JS. Works smoothly on restricted internet connections.
- **Live Highlighting:** See your matches instantly as you type.
- **Multiple Test Cases:** Add and manage independent text boxes to test against different scenarios.
- **Capture Groups Visualization:** Automatically extracts and color-codes regex groups in a side panel.
- **Code Snippet Generator:** Instantly generates boilerplate code for JavaScript, Python, PHP, Java, and C#.
- **Built-in Cheatsheet:** A comprehensive regex reference guide included within the UI.
- **Dark Mode:** Eye-friendly interface designed with pure CSS.

### How to Use
1. Clone this repository or download the `index.html` file.
2. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
3. Type your regex pattern and test texts.

### Screenshots
![Main Interface](Screen-Shots/index1.png)
![Secondary Interface](Screen-Shots/index2.png)

*(Note: Ensure your screenshots are placed in the `Screen-Shots` directory).*

---

## 📚 The Complete Regex Guide

> 💡 **Tip:** Clone the repository and open `index.html` to test all the patterns below interactively!

### What is a Regular Expression?
A regular expression is a sequence of characters that forms a search pattern. When you search for data in a text, you can use this search pattern to describe what you are searching for. It can be a single character or a more complicated pattern.

### JavaScript RegExp Flags
Flags are added to the end of a regex pattern (e.g., `/pattern/g`) to modify its behavior.

| Flag | Description | Example |
| :--- | :--- | :--- |
| `g` | **Global:** Find all matches rather than stopping after the first match. | `/hello/g` |
| `i` | **Ignore Case:** Case-insensitive search. | `/hello/i` |
| `m` | **Multiline:** Treat beginning (`^`) and end (`$`) characters to work over multiple lines. | `/^hello/m` |
| `s` | **DotAll:** Allows `.` to match newline characters. | `/hello.world/s` |
| `u` | **Unicode:** Treat pattern as a sequence of Unicode code points. | `/^\u{1D306}$/u` |
| `v` | **Unicode Sets:** Upgrade to the `u` flag, enables string properties and set operations. | `/[\p{ASCII}&&\p{Letter}]/v` |
| `y` | **Sticky:** Matches only from the index indicated by the `lastIndex` property. | `/hello/y` |
| `d` | **Indices:** Generates indices for substring matches. | `/foo/d` |

### RegExp Group Modifiers
*(Supported in ECMAScript $2025$)*
You can modify flags inline for specific groups using `(?flag:pattern)` or `(?-flag:pattern)`.

| Syntax | Description | Example |
| :--- | :--- | :--- |
| `(?i)` | Turn on case-insensitive matching. | `(?i)hello` |
| `(?-i)` | Turn off case-insensitive matching. | `(?-i)hello` |
| `(?i:...)`| Apply case-insensitive to a specific group. | `(?i:hello) world` |

### JavaScript Regex Flag Properties
These are read-only boolean properties on a RegExp object in JavaScript:
- `global`, `ignoreCase`, `multiline`, `dotAll`, `unicode`, `unicodeSets`, `sticky`, `hasIndices`.

### Regular Expression Methods

**String Methods:**
- `match()`: Returns an array containing all matches.
- `matchAll()`: Returns an iterator containing all matches (including groups).
- `replace()`: Replaces a matched substring with a replacement string.
- `replaceAll()`: Replaces all matched substrings.
- `search()`: Tests for a match and returns the index.
- `split()`: Splits a string into an array of substrings.

**RegExp Methods:**
- `exec()`: Executes a search and returns an array of information (or `null`).
- `test()`: Tests for a match and returns `true` or `false`.

### RegExp Character Classes

| Syntax | Description |
| :--- | :--- |
| `[abc]` | Matches any of the characters `a`, `b`, or `c`. |
| `[^abc]` | Matches any character *except* `a`, `b`, or `c`. |
| `[a-z]` | Matches any character from lowercase `a` to lowercase `z`. |
| `[A-Z]` | Matches any character from uppercase `A` to uppercase `Z`. |
| `[0-9]` | Matches any digit from $0$ to $9$. |
| `[^0-9]`| Matches any non-digit character. |

### RegExp Metacharacters

| Metacharacter | Description |
| :--- | :--- |
| `.` | Find a single character, except newline or line terminator. |
| `\w` | Find a word character (alphanumeric & underscore). |
| `\W` | Find a non-word character. |
| `\d` | Find a digit. |
| `\D` | Find a non-digit character. |
| `\s` | Find a whitespace character. |
| `\S` | Find a non-whitespace character. |
| `\b` | Find a match at the beginning/end of a word. |
| `\B` | Find a match, but NOT at the beginning/end of a word. |
| `\0` | Find a NULL character. |
| `\n` | Find a new line character. |
| `\t` | Find a tab character. |

### RegExp Assertions (Anchors & Boundaries)

| Assertion | Description |
| :--- | :--- |
| `^` | Matches the beginning of input. |
| `$` | Matches the end of input. |
| `(?=...)` | **Positive Lookahead:** Matches if followed by the pattern. |
| `(?!...)` | **Negative Lookahead:** Matches if NOT followed by the pattern. |
| `(?<=...)`| **Positive Lookbehind:** Matches if preceded by the pattern. |
| `(?<!...)`| **Negative Lookbehind:** Matches if NOT preceded by the pattern. |

### RegExp Quantifiers

| Quantifier | Description |
| :--- | :--- |
| `n+` | Matches any string that contains at least one $n$. |
| `n*` | Matches any string that contains zero or more occurrences of $n$. |
| `n?` | Matches any string that contains zero or one occurrences of $n$. |
| `n{X}` | Matches any string that contains a sequence of $X$ $n$'s. |
| `n{X,Y}` | Matches any string that contains a sequence of $X$ to $Y$ $n$'s. |
| `n{X,}` | Matches any string that contains a sequence of at least $X$ $n$'s. |
| `n+?` | Lazy one or more (matches as few as possible). |

### RegExp Groups

| Syntax | Description |
| :--- | :--- |
| `(x)` | **Capturing Group:** Matches `x` and remembers the match. |
| `(?<Name>x)` | **Named Capturing Group:** Matches `x` and stores it under "Name". |
| `(?:x)` | **Non-Capturing Group:** Matches `x` but does not remember the match. |

---

## 🛠 Common Regex Patterns

#### 1. Iran Phone Number (Mobile)
```regex
^(?:0|98|\+98)?9\d{9}$
```
#### 2. Email Address Validation
```regex
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```
#### 3. Username ($3$ to $16$ characters)
```regex
^[a-zA-Z0-9_]{3,16}$
```
#### 4. Strong Password (min $8$ chars, $1$ letter, $1$ number)
```regex
^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$
```
#### 5. OTP / Verification Code ($4$ to $6$ digits)
```regex
^\d{4,6}$
```
#### 6. National ID (Iran)
```regex
^\d{10}$
```
---

## 💻 Using Regex in Programming Languages

### JavaScript
```javascript
const text = "Found 404 errors";
const regex = /\d+/g;
console.log(text.match(regex)); // Output: ["404"]
```
### Python
```python
import re
text = "Found 404 errors"
matches = re.findall(r"\d+", text)
print(matches) # Output: ['404']
```
### PHP
```php
$text = "Found 404 errors";
preg_match_all("/\d+/", $text, $matches);
print_r($matches[0]); // Output: Array ( [0] => 404 )
```
### Java
```java
import java.util.regex.*;

public class Main {
    public static void main(String[] args) {
        String text = "Found 404 errors";
        Matcher matcher = Pattern.compile("\\d+").matcher(text);
        while (matcher.find()) {
            System.out.println(matcher.group()); // Output: 404
        }
    }
}
```
### C#
```csharp
using System;
using System.Text.RegularExpressions;

class Program {
    static void Main() {
        string text = "Found 404 errors";
        foreach (Match match in Regex.Matches(text, @"\d+")) {
            Console.WriteLine(match.Value); // Output: 404
        }
    }
}
```
---

## 👤 Author & Credits

- **Author:** Iliya Esmaeili
- **Contact:** [i.esmaeili@mail.sbu.ac.ir](mailto:i.esmaeili@mail.sbu.ac.ir)
- **Generation:** Documentation structure, technical data, and formatting generated with Google Gemini.

چرا دکمه های table of contents ;کار نمیکنه ؟ 
