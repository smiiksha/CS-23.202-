# Java Programming Lab Programs (1–25)

This repository contains Java Programming Lab programs from Program 1 to Program 25, written in Java and compatible with NetBeans IDE.

Each program includes source code and output screenshots.

---

# Index

1. [Program 1 - Basic Arithmetic Operations Class](#program-1---basic-arithmetic-operations-class)  
2. [Program 2 - Addition of Two Distances (m, cm, mm)](#program-2---addition-of-two-distances-m-cm-mm)  
3. [Program 3 - Addition of Two Times (hr, min, sec)](#program-3---addition-of-two-times-hr-min-sec)  
4. [Program 4 - Addition of Two Distances (m, cm)](#program-4---addition-of-two-distances-m-cm)  
5. [Program 5 - Addition of Two Times (hr, min)](#program-5---addition-of-two-times-hr-min)  
6. [Program 6 - Reverse a 1D Array](#program-6---reverse-a-1d-array)  
7. [Program 7 - Matrix Operations](#program-7---matrix-operations)  
8. [Program 8 - Classic C Programs Converted to Java OOP](#program-8---classic-c-programs-converted-to-java-oop)  
9. [Program 9 - Method Overriding](#program-9---method-overriding-with-parent-class-reference)  
10. [Program 10 - Java Swing Draw and Fill Shapes](#program-10---java-swing--draw-and-fill-shapes)  
11. [Program 11 - Java Swing Calculator GUI](#program-11---java-swing--simple-calculator-gui)  
12. [Program 12 - Java Swing Freehand Drawing App](#program-12---java-swing--freehand-drawing-app)  
13. [Program 13 - Division Class with Exception Handling](#program-13---division-class-with-exception-handling)  

---

# Program 1 - Basic Arithmetic Operations Class

A class with four methods add, subtract, multiply and divide.

```java
public class Arithmetic {

    public int add(int a, int b) {
        return a + b;
    }

    public int subtract(int a, int b) {
        return a - b;
    }

    public int multiply(int a, int b) {
        return a * b;
    }

    public double divide(int a, int b) {
        if (b == 0) {
            System.out.println("Division by zero not allowed!");
            return 0;
        }
        return (double) a / b;
    }

    public static void main(String[] args) {
        Arithmetic obj = new Arithmetic();
        int a = 20, b = 4;

        System.out.println("Add: " + obj.add(a, b));
        System.out.println("Subtract: " + obj.subtract(a, b));
        System.out.println("Multiply: " + obj.multiply(a, b));
        System.out.println("Divide: " + obj.divide(a, b));
    }
}
