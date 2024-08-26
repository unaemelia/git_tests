# Git Tests with GitHub Actions

This is a simple C# project that implements a basic calculator with four fundamental arithmetic operations: addition, subtraction, multiplication, and division.

## Features

- **Addition**: Adds two integers and returns the result.
- **Subtraction**: Subtracts the second integer from the first and returns the result.
- **Multiplication**: Multiplies two integers and returns the result.
- **Division**: Divides the first integer by the second and returns the result.

## Files

### 1. `Calculator.cs`

This file contains the implementation of the `Calculator` class with the following methods:

- `int Add(int a, int b)`: Returns the sum of `a` and `b`.
- `int Subtract(int a, int b)`: Returns the difference when `b` is subtracted from `a`.
- `int Multiply(int a, int b)`: Returns the product of `a` and `b`.
- `int Division(int a, int b)`: Returns the quotient when `a` is divided by `b`.

### 2. `.github/workflows/tests.yml`

This file defines a GitHub Actions workflow for running unit tests on the project. The workflow is triggered on each push to the `main` branch and performs the following steps:

- **Checkout code**: Uses `actions/checkout@v3` to check out the repository code.
- **Set up .NET**: Uses `actions/setup-dotnet@v3` to install .NET 6.x.
- **Restore dependencies**: Runs `dotnet restore` to restore the project dependencies.
- **Run unit tests**: Executes `dotnet test` to run the unit tests and ensure the code is working as expected.
