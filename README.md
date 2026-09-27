# AI Tools Lab

AI Tools Lab is a small, dependency-free Python project for learning and
experimenting with practical programming fundamentals. The repository is
currently a collection of standalone scripts rather than an installable
package.

## What's included

- `SORTING.py` contains a **bubble sort** implementation in `bubble_sort`. The
  function sorts a list in place and returns `None`. The file currently has an
  unresolved `=======` line, however, so Python raises a `SyntaxError` before
  the function can be run.
- `FEATURE-UTILS` contains three utility functions: `is_palindrome`,
  `count_words`, and `celsius_to_fahrenheit`. The file has no `.py` extension,
  so it is loaded by path in the example below.
- `hello.py` prints a short greeting.

## Requirements

- Python 3
- No third-party dependencies

## Installation

Clone the repository and move into its directory:

```bash
git clone https://github.com/mahabir24/ai-tools-lab.git
cd ai-tools-lab
```

## Usage

After removing the unresolved `=======` line from `SORTING.py`, the sorting
function can be called from another Python script as shown. The module also
contains a sample that runs when the file is executed or imported.

```python
from SORTING import bubble_sort

numbers = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(numbers)
print(numbers)
# [11, 12, 22, 25, 34, 64, 90]
```

The utility file can be used as-is and loaded by path with Python's
standard-library `runpy` module:

```python
import runpy

utils = runpy.run_path("FEATURE-UTILS")
is_palindrome = utils["is_palindrome"]
count_words = utils["count_words"]
celsius_to_fahrenheit = utils["celsius_to_fahrenheit"]

print(is_palindrome("A man, a plan, a canal: Panama"))  # True
print(count_words("The quick  brown fox"))  # 4
print(celsius_to_fahrenheit(0))  # 32.0
```

Run the greeting script with `python hello.py`. The utility file's doctests
can be run with `python FEATURE-UTILS`.

## Contributors

- [mahabir24](https://github.com/mahabir24) — repository owner

## MIT License

Copyright (c) 2026 mahabir24

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
