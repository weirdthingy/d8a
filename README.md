# d8a

**d8a** (pronounced *data*) is a highly restrictive, single-line register-based esoteric programming language built to maximize developer suffering and architectural puzzle-solving. 

Developed by **weirdthingy**, d8a strips away standard programming luxuries, turning every variable manipulation and conditional flow into a complex mathematical puzzle.

## Core Mechanics

1. **The 8 Registers:** You only have 8 internal variables initialized at 0: `a, b, c, d, e, f, g, h`.
2. **The Single-Digit Restraint:** You can only modify registers using a **single digit (0-9)** per math command. Want to reach high ASCII characters? You must multiply and add your way up step-by-step.
3. **The Anti-Copy-Paste Fog:** The moment your program finishes execution, the entire source code is instantly wiped from the terminal screen using native cross-platform handlers. You see only the output; the code is gone forever.
4. **The Silent Tax:** Errors such as dividing by zero or syntax corruption are swallowed completely in absolute silence. The interpreter will not crash; it will simply stay mute, forcing you to manually debug your single line.

---

## Syntax Guide 

### Math Operations
* `{num}+{var}` - Add a single-digit quantity to a variable (e.g., `5+a`).
* `{num}-{var}` - Subtract a single-digit quantity from a variable (e.g., `2-b`).
* `{num}*{var}` - Multiply a variable by a single-digit quantity (e.g., `9*c`).
* `{num}//{var}` - Integer division of a variable by a single-digit quantity (e.g., `3//d`).

### Input & Symmetrical Output
* `!{var}!` - Prompt the user for an integer input and save it to the register.
* `/{var}/` - Print the ASCII char of a variable (no newline).
* `({var})` - Print the ASCII char of a variable (with newline).
* `={var}=` - Print the raw integer value of a variable (no newline).
* `#{var}#` - Print the raw integer value of a variable (with newline).

### Debt Control (Conditionals)
* `?{var}{value}` - Checks if the register matches the target value.
* `$` - *"You owe me the action"*. Executes the immediate next token if the previous `?` condition was **True**.
* `$$` - *"Double or nothing"*. The **Else** handler. Executes the immediate next token if the previous `?` condition was **False**.

### Functional Macros
* `<w {commands}>` - Define a reusable functional sequence inside the macro buffer `w` (one definition allowed at a time).
* `<w>` - Execute the stored macro components. Empty macros execute in absolute silence.

---

## Code Examples

### Symmetrical Logic Validation (Conditional Function Challenge)
```text
!a! <w 2*a #a#> ?a7 $<w> $$#b#
```

---
*Proudly compiled via embedded Blender Python runtimes.*
