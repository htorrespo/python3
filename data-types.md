# Strings

<!-- K:\usuario\Downloads\book.programming_in_python_3.summerfield.pdf -->
65 pp

Strings are represented by the immutable str data type which holds a sequence
of Unicode characters. The str data type can be called as a function to create
string objects—with no arguments it returns an empty string, with a nonstring
argument it returns the string form of the argument, and with a string
argument it returns a copy of the string. The str() function can also be used
as a conversion function, in which case the first argument should be a string
or something convertable to a string, with up to two optional string arguments
being passed, one specifying the encoding to use and the other specifying how
to handle encoding errors.

Earlier we mentioned that string literals are created using quotes, and that we
are free to use single or double quotes providing we use the same at both ends.
In addition,we can use a triple quoted string—this is Python-speak for a string
that begins and ends with three quote characters (either three single quotes or
three double quotes). For example:

```python
text = """A triple quoted string like this can include 'quotes' and
"quotes" without formality. We can also escape newlines \
so this particular string is actually only two lines long."""
```

Python’s String Escapes

```
Escape Meaning
\newline Escape (i.e., ignore) the newline
\\ Backslash (\)
\' Single quote (’)
\" Double quote (")
\a ASCII bell (BEL)
\b ASCII backspace (BS)
\f ASCII formfeed (FF)
\n ASCII linefeed (LF)
\N{name} Unicode character with the given name
\ooo Character with the given octal value
\r ASCII carriage return (CR)
\t ASCII tab (TAB)
\uhhhh Unicode character with the given 16-bit hexadecimal value
\Uhhhhhhhh Unicode character with the given 32-bit hexadecimal value
\v ASCII vertical tab (VT)
\xhh Character with the given 8-bit hexadecimal value
```

If we want to use quotes inside a normal quoted string we can do so without
formality if they are different from the delimiting quotes; otherwise, we must
escape them:

```python
a = "Single 'quotes' are fine; \"doubles\" must be escaped."
b = 'Single \'quotes\' must be escaped; "doubles" are fine.'
```

Python uses newline as its statement terminator, except inside parentheses
(()), square brackets ([]), braces ({}), or triple quoted strings. Newlines can be
used without formality in triple quoted strings, and we can include newlines
in any string literal using the \n escape sequence. All of Python’s escape sequences
are shown in Table 2.7.In some situations—for example,when writing
regular expressions—we need to create strings with lots of literal backslashes.
(Regular expressions are the subject of Chapter 13.) This can be inconvenient
since each one must be escaped:

```python
import re
phone1 = re.compile("^((?:[(]\\d+[)])?\\s*\\d+(?:-\\d+)?)$")
```
