# Advanced Calculus Solver

A powerful, user-friendly application for solving complex calculus expressions, including derivatives, integrals, and limits.

## Features

- **Comprehensive Calculus Operations**:

  - Derivatives (including partial derivatives and higher-order derivatives)
  - Integrals (both indefinite and definite)
  - Limits
  - Combined operations in a single expression

- **User-Friendly Interface**:

  - Clean, professional design
  - Mathematical symbol selector for easy input
  - Clear button for quick expression reset
  - Step-by-step solution display

- **Advanced Parsing**:
  - Automatic multiplication detection (e.g., "2x" is interpreted as "2\*x")
  - Support for complex mathematical expressions
  - Robust error handling with helpful messages

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/advanced-calculus-solver.git
   cd advanced-calculus-solver
   ```

2. Create and activate a virtual environment (recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the application:

```bash
streamlit run combined_calculus_solver.py
```

The application will open in your default web browser.

## Expression Syntax

### Derivatives

- Basic derivative: `d/dx(x^2)`
- Higher-order derivative: `d^2/dx^2(x^3)`
- Partial derivative: `d/dy(x^2 + y^2)`

### Integrals

- Indefinite integral: `∫x^2 dx`
- Definite integral: `∫(1,2)x^2 dx`

### Limits

- Basic limit: `lim(x->0)(sin(x)/x)`
- Limit at infinity: `lim(x->oo)(1/x)`

### Combined Operations

- `∫d/dx(x^2) dx`
- `d/dx(∫x^2 dx)`
- `lim(x->0)(d/dx(sin(x)))`

## Example Expressions

- `x^2/(2x+3x^2)` (automatically converted to `x^2/(2*x+3*x^2)`)
- `2x^2 + 3x + 1` (automatically converted to `2*x^2 + 3*x + 1`)
- `(x+1)(x-1)` (automatically converted to `(x+1)*(x-1)`)
- `sin(x)/x` (for limits as x approaches 0)

## Dependencies

- **streamlit**: For the web interface
- **sympy**: For symbolic mathematics and calculus operations
- **re**: For regular expression parsing
