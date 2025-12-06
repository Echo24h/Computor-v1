# Computor v1
Computor v1 is a simple program to solve polynomial equations up to degree 2, showing the reduced form, degree, and solutions.

## Usage

```bash
# With argument
python computor "5 * X^0 + 4 * X^1 - 9.3 * X^2 = 1 * X^0"

# Interactive mode
python computor
```

## Examples

### Quadratic equation (positive discriminant)
```bash
$ python computor "5 * X^0 + 4 * X^1 - 9.3 * X^2 = 1 * X^0"
Reduced form: 4.0 * X^0 + 4.0 * X^1 - 9.3 * X^2 = 0
Polynomial degree: 2
Discriminant is strictly positive, the two solutions are:
0.905239
-0.475131
```

### Linear equation
```bash
$ python computor "5 * X^0 + 4 * X^1 = 4 * X^0"
Reduced form: 1.0 * X^0 + 4.0 * X^1 = 0
Polynomial degree: 1
The solution is:
-0.25
```

### Complex solutions (negative discriminant)
```bash
$ python computor "1 * X^0 + 2 * X^1 + 5 * X^2 = 0"
Reduced form: 1.0 * X^0 + 2.0 * X^1 + 5.0 * X^2 = 0
Polynomial degree: 2
Discriminant is strictly negative, the two complex solutions are:
-0.2 + 0.4i
-0.2 - 0.4i
```

### Degree > 2
```bash
$ python computor "8 * X^0 - 6 * X^1 + 0 * X^2 - 5.6 * X^3 = 3 * X^0"
Reduced form: 5.0 * X^0 - 6.0 * X^1 + 0.0 * X^2 - 5.6 * X^3 = 0
Polynomial degree: 3
The polynomial degree is strictly greater than 2, I can't solve.
```

### Special cases
```bash
# Infinite solutions
$ python computor "6 * X^0 = 6 * X^0"
Reduced form: 0.0 * X^0 = 0
Polynomial degree: 0
Any real number is a solution.

# No solution
$ python computor "10 * X^0 = 15 * X^0"
Reduced form: -5.0 * X^0 = 0
Polynomial degree: 0
No solution.
```

## Input Format

Equations must follow this format:
- Terms: `coefficient * X^degree`
- Example: `5 * X^2 + 3 * X^1 - 2 * X^0 = 0`
- Spaces are optional
- Coefficients can be decimals: `3.14 * X^2`
- Signs: `+` or `-`

## Requirements

- Python 3.x
- No external dependencies