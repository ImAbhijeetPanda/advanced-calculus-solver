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

### Option 1: Run Locally

Run the application on your local machine:

```bash
streamlit run combined_calculus_solver.py
```

The application will open in your default web browser.

### Option 2: Use the Deployed Version

Access the live version of the application directly at:

[https://advanced-calculus.streamlit.app/](https://advanced-calculus.streamlit.app/)

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

## Technical Approach

### Architecture

The Advanced Calculus Solver is built using a modular architecture that separates concerns:

1. **User Interface Layer** (Streamlit)

   - Provides an intuitive interface for expression input
   - Displays results in a clean, formatted manner
   - Offers symbol selection for complex mathematical notation

2. **Expression Parsing Layer**

   - Implements regex-based parsing to handle implicit multiplication
   - Converts user-friendly notation to SymPy-compatible format
   - Validates input expressions before processing

3. **Computational Core** (SymPy)
   - Performs symbolic mathematics operations
   - Handles calculus operations (derivatives, integrals, limits)
   - Simplifies expressions for cleaner output

### Key Implementation Features

1. **Unified Expression Handling**

   - Single input field that intelligently detects operation type
   - Pattern recognition for derivatives, integrals, and limits
   - Support for nested operations (e.g., derivative of an integral)

2. **Automatic Multiplication Detection**

   - Converts expressions like "2x" to "2\*x" automatically
   - Handles complex cases like "(x+1)(x-1)" → "(x+1)\*(x-1)"
   - Preserves function notation (e.g., "sin(x)" remains unchanged)

3. **Error Handling**
   - Provides meaningful error messages for invalid expressions
   - Gracefully handles edge cases and syntax errors
   - Guides users toward correct syntax

### Performance Considerations

- Lazy evaluation of expressions to improve performance
- Caching of results to avoid redundant calculations
- Efficient parsing algorithms to handle complex expressions

## Credits

This project is authored and maintained by **[Abhijeet Panda](https://github.com/ImAbhijeetPanda)**.

## Contact

For any questions or feedback, feel free to reach out:

- **Email**: [iamabhijeetpanda@gmail.com](mailto:iamabhijeetpanda@gmail.com)
- **LinkedIn**: [Abhijeet Panda](https://www.linkedin.com/in/imabhijeetpanda)
- **GitHub**: [ImAbhijeetPanda](https://github.com/ImAbhijeetPanda)
