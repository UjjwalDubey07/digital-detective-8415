# Mission 5: Numbers and Data

## Task 5.1 — Convert Numbers by Hand

| Question | Working & Answer |
| :--- | :--- |
| Convert decimal 13 to binary | 13÷2=6 r1, 6÷2=3 r0, 3÷2=1 r1, 1÷2=0 r1 → **1101** |
| Convert decimal 25 to binary | 25÷2=12 r1, 12÷2=6 r0, 6÷2=3 r0, 3÷2=1 r1, 1÷2=0 r1 → **11001** |
| Convert binary 1010 to decimal | 1×2³+0×2²+1×2¹+0×2⁰ = 8+0+2+0 = **10** |
| Convert binary 1101 to decimal | 1×2³+1×2²+0×2¹+1×2⁰ = 8+4+0+1 = **13** |
| Convert hexadecimal A to decimal | A = **10** |
| Convert hexadecimal 1F to decimal | 1×16¹ + 15×16⁰ = 16+15 = **31** |
| Convert binary 1111 to hexadecimal | 1111₂ = F₁₆ → **F** |

---

## Task 5.2 — Verify Using Python

**Commands:** `python3` (interactive REPL)

| Expression Tested | Result | Matches Manual? |
| :--- | :--- | :--- |
| `bin(13)` | `'0b1101'` | ✅ Yes (1101) |
| `bin(25)` | `'0b11001'` | ✅ Yes (11001) |
| `int('1010', 2)` | `10` | ✅ Yes |
| `int('1101', 2)` | `13` | ✅ Yes |
| `hex(10)` | `'0xa'` | ✅ Yes (A) |
| `hex(31)` | `'0x1f'` | ✅ Yes (1F) |
| `int('A', 16)` | `10` | ✅ Yes |
| `int('1F', 16)` | `31` | ✅ Yes |
| `hex(int('1111', 2))` | `'0xf'` | ✅ Yes (F) |

---

## Task 5.3 — Build a Number Converter

**File:** `mission-05-numbers-data/number_converter.py`

```python
# number_converter.py
user_input = int(input("Enter a positive decimal integer: "))

binary = bin(user_input)
hexadecimal = hex(user_input)

print(f"Binary:    {binary}")
print(f"Hexadecimal: {hexadecimal}")


Test runs:

┌─────────────┬───────────────┬────────────────────┐
│ Test Number │ Binary Output │ Hexadecimal Output │
├─────────────┼───────────────┼────────────────────┤
│ 13          │ 1101          │ D                  │
├─────────────┼───────────────┼────────────────────┤
│ 255         │ 11111111      │ FF                 │
├─────────────┼───────────────┼────────────────────┤
│ 1024        │ 10000000000   │ 400                │
└─────────────┴───────────────┴────────────────────┘

Explanation of conversion functions:
- bin(n) converts an integer to its binary string representation prefixed with '0b'.
- hex(n) converts an integer to its hexadecimal string representation prefixed with '0x'. 

---

Task 5.4 — How Is Text Stored?

1. ASCII code for 'A': 65
   ASCII code for 'a': 97
2. Why encoding standards?
   Computers store only bits. An encoding standard provides a consistent mapping between characters and numeric codes so that text can be reliably stored, transmitted, and displayed across different systems. Without a shared standard, the same byte sequence would render as different characters on different systems.
3. Character not in basic ASCII:
   € (Euro sign, Unicode U+20AC) — basic ASCII only covers 0–127 (English letters, digits, punctuation).

---

Mission 5 Summary & Reflection

- Files created: number_converter.py
- Commands used: python3 (REPL), python3 number_converter.py
- Python functions: bin(), hex(), int(string, base), input(), print(), f-strings
- Key concepts: Base conversion (2, 10, 16), positional notation, character encoding (ASCII vs UTF-8), Python built-in conversion functions.
- Challenges & Resolution: ["No major issues."]
