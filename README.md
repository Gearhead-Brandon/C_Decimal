# Decimal Summary  

## Overview  
The **s21_decimal** project involves creating a custom `decimal` type in C for precise financial calculations. It minimizes floating-point errors by using a **96-bit integer** and a **scaling factor** for decimal places.  

## Decimal Structure  
The `s21_decimal` type consists of an **array of four 32-bit integers (`int bits[4]`)**:  
- **bits[0], bits[1], bits[2]** – store the 96-bit integer value.  
- **bits[3]** – contains:  
  - **Bits 0-15**: Unused (must be 0).  
  - **Bits 16-23**: Exponent (0-28), defining decimal places.  
  - **Bits 24-30**: Unused (must be 0).  
  - **Bit 31**: Sign (0 for positive, 1 for negative).  

## Functionality  
The library includes:  
- **Arithmetic operations**: Addition, subtraction, multiplication, division.  
- **Comparison operations**: Equal, greater/less than, etc.  
- **Conversions**: From/to `int` and `float`.  
- **Rounding functions**: Floor, round, truncate, negate.  

The implementation follows **structured programming**, uses **unit tests** with **Check**, and provides a **Makefile** for compilation and testing.  