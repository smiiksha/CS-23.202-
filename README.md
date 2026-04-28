☕ CS-23.202 — Java Laboratory
B.Tech 2nd Year | Mody University of Science & Technology
Show Image
Show Image
Show Image

📋 About
This repository contains all lab assignments for the Java Programming Laboratory (CS-23.202) course, 2nd Year B.Tech, AI & Data Science — Mody University of Science & Technology. Each program demonstrates core Object-Oriented Programming concepts in Java.

📂 Assignment Index
#Title01Write a class with four methods add, subtract, multiply and divide and test all the methods in the main02Write a class for addition of two distances where each distance is given in mm, cm, m03Write a class for addition of two times where each time is given in hr, min, sec04Write a class for addition of two distances where each distance is given in m and cm05Write a class for addition of two times where each time is given in hr and min06Write a class with necessary methods to reverse a 1D array07Write a class with necessary methods for matrix operations: transpose, addition, multiplication, sum of rows, columns, and diagonals08Collect all 5 codes of C language (Factorial, Armstrong, Palindrome, Fibonacci, Prime) and convert them into object-oriented Java09Method overriding with parent class reference — Animal, Dog, Cat10Java Swing — Draw and fill shapes (rectangle and oval) with color buttons11Java Swing — Simple Calculator GUI with two inputs and +, -, *, / buttons12Java Swing — Freehand Drawing App with color buttons and brush size slider13Division class with integer division, float division, remainder, and batch division — all with exception handling14Student Registration Form using Java Swing and JDBC (MySQL)15JFrame with 10 buttons each performing a different functionality16Three classes (A, B, C) each printing 1 to 100 along with the class name17Three classes printing 1 to 10 sequentially without threads18Three classes printing 1 to 10 using the Runnable interface19File copy using Byte Stream and Character Stream20ArrayList operations: add, remove, search, update, and iteration21LinkedList operations: insert at beginning, middle, end, delete, search, display22Stack operations using Java Collections Framework23HashMap operations: insert, retrieve, remove, and iterate key-value pairs24TreeMap operations: insert, display in sorted order, search, and remove25Stack implementation using arrays with overflow and underflow handling

💻 Assignments

Assignment 1
Write a class with four methods add, subtract, multiply and divide and test all the methods in the main.
CodeOutput```javapublic class Arithmetic {
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

---

### Assignment 2

**Write a class for addition of two distances where each distance is given in mm, cm, m.**

| Code | Output |
| --- | --- |
| ```java
public class Distance3 {
    int meters, centimeters, millimeters;

    Distance3(int m, int cm, int mm) {
        this.meters = m;
        this.centimeters = cm;
        this.millimeters = mm;
    }

    public static Distance3 add(Distance3 d1, Distance3 d2) {
        int totalMM = d1.millimeters + d2.millimeters;
        int totalCM = d1.centimeters + d2.centimeters + totalMM / 10;
        totalMM = totalMM % 10;
        int totalM = d1.meters + d2.meters + totalCM / 100;
        totalCM = totalCM % 100;
        return new Distance3(totalM, totalCM, totalMM);
    }

    public void display() {
        System.out.println(meters + " m, " + centimeters + " cm, " + millimeters + " mm");
    }

    public static void main(String[] args) {
        Distance3 d1 = new Distance3(3, 75, 8);
        Distance3 d2 = new Distance3(2, 45, 6);
        System.out.print("Distance 1: "); d1.display();
        System.out.print("Distance 2: "); d2.display();
        Distance3 result = Distance3.add(d1, d2);
        System.out.print("Sum: "); result.display();
    }
}
``````````````````````````| *(add output screenshot here)* |

---

### Assignment 3

**Write a class for addition of two times where each time is given in hr, min, sec.**

| Code | Output |
| --- | --- |
| ```java
public class Time3 {
    int hours, minutes, seconds;

    Time3(int h, int m, int s) {
        this.hours = h;
        this.minutes = m;
        this.seconds = s;
    }

    public static Time3 add(Time3 t1, Time3 t2) {
        int totalSec = t1.seconds + t2.seconds;
        int totalMin = t1.minutes + t2.minutes + totalSec / 60;
        totalSec = totalSec % 60;
        int totalHr = t1.hours + t2.hours + totalMin / 60;
        totalMin = totalMin % 60;
        return new Time3(totalHr, totalMin, totalSec);
    }

    public void display() {
        System.out.println(hours + " hr, " + minutes + " min, " + seconds + " sec");
    }

    public static void main(String[] args) {
        Time3 t1 = new Time3(2, 45, 50);
        Time3 t2 = new Time3(1, 30, 25);
        System.out.print("Time 1: "); t1.display();
        System.out.print("Time 2: "); t2.display();
        Time3 result = Time3.add(t1, t2);
        System.out.print("Sum: "); result.display();
    }
}
`````````````````````````| *(add output screenshot here)* |

---

### Assignment 4

**Write a class for addition of two distances where each distance is given in m and cm.**

| Code | Output |
| --- | --- |
| ```java
public class Distance2 {
    int meters, centimeters;

    Distance2(int m, int cm) {
        this.meters = m;
        this.centimeters = cm;
    }

    public static Distance2 add(Distance2 d1, Distance2 d2) {
        int totalCM = d1.centimeters + d2.centimeters;
        int totalM = d1.meters + d2.meters + totalCM / 100;
        totalCM = totalCM % 100;
        return new Distance2(totalM, totalCM);
    }

    public void display() {
        System.out.println(meters + " m, " + centimeters + " cm");
    }

    public static void main(String[] args) {
        Distance2 d1 = new Distance2(5, 80);
        Distance2 d2 = new Distance2(3, 60);
        System.out.print("Distance 1: "); d1.display();
        System.out.print("Distance 2: "); d2.display();
        Distance2 result = Distance2.add(d1, d2);
        System.out.print("Sum: "); result.display();
    }
}
````````````````````````| *(add output screenshot here)* |

---

### Assignment 5

**Write a class for addition of two times where each time is given in hr and min.**

| Code | Output |
| --- | --- |
| ```java
public class Time2 {
    int hours, minutes;

    Time2(int h, int m) {
        this.hours = h;
        this.minutes = m;
    }

    public static Time2 add(Time2 t1, Time2 t2) {
        int totalMin = t1.minutes + t2.minutes;
        int totalHr = t1.hours + t2.hours + totalMin / 60;
        totalMin = totalMin % 60;
        return new Time2(totalHr, totalMin);
    }

    public void display() {
        System.out.println(hours + " hr, " + minutes + " min");
    }

    public static void main(String[] args) {
        Time2 t1 = new Time2(3, 50);
        Time2 t2 = new Time2(2, 40);
        System.out.print("Time 1: "); t1.display();
        System.out.print("Time 2: "); t2.display();
        Time2 result = Time2.add(t1, t2);
        System.out.print("Sum: "); result.display();
    }
}
```````````````````````| *(add output screenshot here)* |

---

### Assignment 6

**Write a class with necessary methods to reverse a 1D array.**

| Code | Output |
| --- | --- |
| ```java
public class ReverseArray {

    public void inputArray(int[] arr) {
        System.out.print("Original Array: ");
        for (int val : arr) System.out.print(val + " ");
        System.out.println();
    }

    public void reverseArray(int[] arr) {
        int left = 0, right = arr.length - 1;
        while (left < right) {
            int temp = arr[left];
            arr[left] = arr[right];
            arr[right] = temp;
            left++;
            right--;
        }
    }

    public void displayArray(int[] arr) {
        System.out.print("Reversed Array: ");
        for (int val : arr) System.out.print(val + " ");
        System.out.println();
    }

    public static void main(String[] args) {
        ReverseArray ra = new ReverseArray();
        int[] arr = {10, 20, 30, 40, 50};
        ra.inputArray(arr);
        ra.reverseArray(arr);
        ra.displayArray(arr);
    }
}
``````````````````````| *(add output screenshot here)* |

---

### Assignment 7

**Write a class with necessary methods for matrix operations: transpose, addition, multiplication, sum of rows, sum of columns, and sum of diagonals.**

| Code | Output |
| --- | --- |
| ```java
public class MatrixOps {
    int rows, cols;
    int[][] matrix;

    MatrixOps(int[][] mat) {
        this.matrix = mat;
        this.rows = mat.length;
        this.cols = mat[0].length;
    }

    public void display() {
        for (int[] row : matrix) {
            for (int val : row) System.out.printf("%5d", val);
            System.out.println();
        }
    }

    public int[][] transpose() {
        int[][] result = new int[cols][rows];
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                result[j][i] = matrix[i][j];
        return result;
    }

    public int[][] add(MatrixOps other) {
        int[][] result = new int[rows][cols];
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                result[i][j] = matrix[i][j] + other.matrix[i][j];
        return result;
    }

    public int[][] multiply(MatrixOps other) {
        int[][] result = new int[rows][other.cols];
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < other.cols; j++)
                for (int k = 0; k < cols; k++)
                    result[i][j] += matrix[i][k] * other.matrix[k][j];
        return result;
    }

    public void sumOfRows() {
        System.out.println("Sum of each row:");
        for (int i = 0; i < rows; i++) {
            int sum = 0;
            for (int j = 0; j < cols; j++) sum += matrix[i][j];
            System.out.println("Row " + (i+1) + ": " + sum);
        }
    }

    public void sumOfCols() {
        System.out.println("Sum of each column:");
        for (int j = 0; j < cols; j++) {
            int sum = 0;
            for (int i = 0; i < rows; i++) sum += matrix[i][j];
            System.out.println("Col " + (j+1) + ": " + sum);
        }
    }

    public void sumOfDiagonals() {
        int mainDiag = 0, antiDiag = 0;
        for (int i = 0; i < rows; i++) {
            mainDiag += matrix[i][i];
            antiDiag += matrix[i][cols - 1 - i];
        }
        System.out.println("Main Diagonal Sum: " + mainDiag);
        System.out.println("Anti Diagonal Sum: " + antiDiag);
    }

    public static void main(String[] args) {
        int[][] m1 = {{1,2,3},{4,5,6},{7,8,9}};
        int[][] m2 = {{9,8,7},{6,5,4},{3,2,1}};
        MatrixOps mat1 = new MatrixOps(m1);
        MatrixOps mat2 = new MatrixOps(m2);

        System.out.println("Matrix 1:"); mat1.display();
        System.out.println("Transpose:"); new MatrixOps(mat1.transpose()).display();
        System.out.println("Addition:"); new MatrixOps(mat1.add(mat2)).display();
        System.out.println("Multiplication:"); new MatrixOps(mat1.multiply(mat2)).display();
        mat1.sumOfRows();
        mat1.sumOfCols();
        mat1.sumOfDiagonals();
    }
}
`````````````````````| *(add output screenshot here)* |

---

### Assignment 8

**Collect all 5 codes of C language (Factorial, Armstrong, Palindrome, Fibonacci, Prime) and convert them into object-oriented Java and test the result in main.**

| Code | Output |
| --- | --- |
| ```java
public class ClassicPrograms {

    // 1. Factorial
    public long factorial(int n) {
        if (n <= 1) return 1;
        return n * factorial(n - 1);
    }

    // 2. Armstrong Number
    public boolean isArmstrong(int num) {
        int temp = num, sum = 0, digits = String.valueOf(num).length();
        while (temp != 0) {
            int d = temp % 10;
            sum += Math.pow(d, digits);
            temp /= 10;
        }
        return sum == num;
    }

    // 3. Palindrome
    public boolean isPalindrome(int num) {
        int reversed = 0, temp = num;
        while (temp != 0) {
            reversed = reversed * 10 + temp % 10;
            temp /= 10;
        }
        return reversed == num;
    }

    // 4. Fibonacci Series
    public void fibonacci(int n) {
        int a = 0, b = 1;
        System.out.print("Fibonacci: ");
        for (int i = 0; i < n; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }
        System.out.println();
    }

    // 5. Prime Number
    public boolean isPrime(int num) {
        if (num < 2) return false;
        for (int i = 2; i <= Math.sqrt(num); i++)
            if (num % i == 0) return false;
        return true;
    }

    public static void main(String[] args) {
        ClassicPrograms cp = new ClassicPrograms();

        System.out.println("Factorial of 6: " + cp.factorial(6));
        System.out.println("153 is Armstrong: " + cp.isArmstrong(153));
        System.out.println("121 is Palindrome: " + cp.isPalindrome(121));
        cp.fibonacci(10);
        System.out.println("17 is Prime: " + cp.isPrime(17));
    }
}
````````````````````| *(add output screenshot here)* |

---

### Assignment 9

**Method overriding with parent class reference — create a parent class Animal and two child classes Dog and Cat, each overriding the sound() method, called via parent reference.**

| Code | Output |
| --- | --- |
| ```java
class Animal {
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog says: Woof!");
    }
}

class Cat extends Animal {
    @Override
    public void sound() {
        System.out.println("Cat says: Meow!");
    }
}

public class OverrideDemo {
    public static void main(String[] args) {
        Animal ref;

        ref = new Dog();
        ref.sound();   // Calls Dog's sound()

        ref = new Cat();
        ref.sound();   // Calls Cat's sound()

        ref = new Animal();
        ref.sound();   // Calls Animal's sound()
    }
}
```````````````````| *(add output screenshot here)* |

---

### Assignment 10

**Java Swing — Draw and fill shapes (rectangle and oval) with options to toggle fill and change colors.**

| Code | Output |
| --- | --- |
| ```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class ShapeDrawer extends JFrame {
    String shape = "Rectangle";
    Color color = Color.RED;
    boolean fill = false;

    DrawPanel panel = new DrawPanel();

    ShapeDrawer() {
        setTitle("Shape Drawer");
        setSize(600, 500);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setLayout(new BorderLayout());

        JPanel controls = new JPanel();
        JButton drawRect = new JButton("Rectangle");
        JButton drawOval = new JButton("Oval");
        JButton fillBtn  = new JButton("Fill");
        JButton red      = new JButton("Red");
        JButton black    = new JButton("Black");

        drawRect.addActionListener(e -> { shape = "Rectangle"; fill = false; panel.repaint(); });
        drawOval.addActionListener(e -> { shape = "Oval";      fill = false; panel.repaint(); });
        fillBtn .addActionListener(e -> { fill = !fill;        panel.repaint(); });
        red     .addActionListener(e -> { color = Color.RED;   panel.repaint(); });
        black   .addActionListener(e -> { color = Color.BLACK; panel.repaint(); });

        controls.add(drawRect); controls.add(drawOval);
        controls.add(fillBtn);  controls.add(red); controls.add(black);

        add(controls, BorderLayout.NORTH);
        add(panel, BorderLayout.CENTER);
        setVisible(true);
    }

    class DrawPanel extends JPanel {
        protected void paintComponent(Graphics g) {
            super.paintComponent(g);
            g.setColor(color);
            if (shape.equals("Rectangle")) {
                if (fill) g.fillRect(150, 100, 250, 150);
                else      g.drawRect(150, 100, 250, 150);
            } else {
                if (fill) g.fillOval(150, 100, 250, 150);
                else      g.drawOval(150, 100, 250, 150);
            }
        }
    }

    public static void main(String[] args) {
        new ShapeDrawer();
    }
}
``````````````````| *(add output screenshot here)* |

---

### Assignment 11

**Java Swing — Simple Calculator GUI that takes two inputs and performs +, -, *, /.**

| Code | Output |
| --- | --- |
| ```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class Calculator extends JFrame {
    JTextField num1 = new JTextField(10);
    JTextField num2 = new JTextField(10);
    JTextField result = new JTextField(15);

    Calculator() {
        setTitle("Simple Calculator");
        setSize(400, 200);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setLayout(new GridLayout(5, 2, 5, 5));

        result.setEditable(false);

        add(new JLabel("Number 1:")); add(num1);
        add(new JLabel("Number 2:")); add(num2);

        JButton add = new JButton("+");
        JButton sub = new JButton("-");
        JButton mul = new JButton("*");
        JButton div = new JButton("/");

        add.addActionListener(e -> compute('+'));
        sub.addActionListener(e -> compute('-'));
        mul.addActionListener(e -> compute('*'));
        div.addActionListener(e -> compute('/'));

        add(add); add(sub); add(mul); add(div);
        add(new JLabel("Result:")); add(result);
        setVisible(true);
    }

    void compute(char op) {
        try {
            double a = Double.parseDouble(num1.getText());
            double b = Double.parseDouble(num2.getText());
            double res = switch (op) {
                case '+' -> a + b;
                case '-' -> a - b;
                case '*' -> a * b;
                case '/' -> b != 0 ? a / b : Double.NaN;
                default  -> 0;
            };
            result.setText(b == 0 && op == '/' ? "Error: Div by 0" : String.valueOf(res));
        } catch (NumberFormatException ex) {
            result.setText("Invalid Input");
        }
    }

    public static void main(String[] args) {
        new Calculator();
    }
}
`````````````````| *(add output screenshot here)* |

---

### Assignment 12

**Java Swing — Freehand Drawing App with color buttons and brush size slider.**

| Code | Output |
| --- | --- |
| ```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class DrawingApp extends JFrame {
    Color drawColor = Color.BLACK;
    int brushSize = 5;
    int prevX = -1, prevY = -1;
    Image canvas;
    Graphics2D g2d;

    DrawingApp() {
        setTitle("Freehand Drawing");
        setSize(700, 550);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setLayout(new BorderLayout());

        JPanel toolbar = new JPanel();
        String[] colors = {"Red", "Black", "Blue", "Magenta"};
        Color[] colorVals = {Color.RED, Color.BLACK, Color.BLUE, Color.MAGENTA};

        for (int i = 0; i < colors.length; i++) {
            final Color c = colorVals[i];
            JButton btn = new JButton(colors[i]);
            btn.addActionListener(e -> drawColor = c);
            toolbar.add(btn);
        }

        JSlider slider = new JSlider(1, 30, 5);
        slider.addChangeListener(e -> brushSize = slider.getValue());
        toolbar.add(new JLabel("Brush:")); toolbar.add(slider);

        JButton clear = new JButton("Clear");
        clear.addActionListener(e -> { g2d.setColor(Color.WHITE); g2d.fillRect(0, 0, 700, 500); repaint(); });
        toolbar.add(clear);

        add(toolbar, BorderLayout.NORTH);

        JPanel drawPanel = new JPanel() {
            public void paintComponent(Graphics g) {
                super.paintComponent(g);
                if (canvas == null) {
                    canvas = createImage(700, 500);
                    g2d = (Graphics2D) canvas.getGraphics();
                    g2d.setColor(Color.WHITE);
                    g2d.fillRect(0, 0, 700, 500);
                }
                g.drawImage(canvas, 0, 0, null);
            }
        };

        drawPanel.addMouseListener(new MouseAdapter() {
            public void mouseReleased(MouseEvent e) { prevX = prevY = -1; }
        });
        drawPanel.addMouseMotionListener(new MouseMotionAdapter() {
            public void mouseDragged(MouseEvent e) {
                if (canvas == null) return;
                g2d.setColor(drawColor);
                g2d.setStroke(new BasicStroke(brushSize));
                if (prevX != -1) g2d.drawLine(prevX, prevY, e.getX(), e.getY());
                prevX = e.getX(); prevY = e.getY();
                drawPanel.repaint();
            }
        });

        add(drawPanel, BorderLayout.CENTER);
        setVisible(true);
    }

    public static void main(String[] args) {
        new DrawingApp();
    }
}
````````````````| *(add output screenshot here)* |

---

### Assignment 13

**Division class with integer division, float division, remainder, and batch division — all with divide-by-zero exception handling.**

| Code | Output |
| --- | --- |
| ```java
public class Division {

    public int intDivide(int a, int b) throws ArithmeticException {
        if (b == 0) throw new ArithmeticException("Integer division by zero!");
        return a / b;
    }

    public double floatDivide(double a, double b) throws ArithmeticException {
        if (b == 0) throw new ArithmeticException("Float division by zero!");
        return a / b;
    }

    public int remainder(int a, int b) throws ArithmeticException {
        if (b == 0) throw new ArithmeticException("Modulo by zero!");
        return a % b;
    }

    public void divideAll(int[] numbers, int divisor) {
        if (divisor == 0) {
            System.out.println("Cannot divide: divisor is zero.");
            return;
        }
        System.out.println("Dividing all by " + divisor + ":");
        for (int num : numbers)
            System.out.println(num + " / " + divisor + " = " + (double) num / divisor);
    }

    public static void main(String[] args) {
        Division d = new Division();

        try {
            System.out.println("Int Divide: " + d.intDivide(20, 4));
            System.out.println("Float Divide: " + d.floatDivide(22.5, 4.5));
            System.out.println("Remainder: " + d.remainder(17, 5));
            d.divideAll(new int[]{10, 20, 30}, 3);

            // Test exception
            System.out.println(d.intDivide(10, 0));
        } catch (ArithmeticException e) {
            System.out.println("Exception caught: " + e.getMessage());
        }
    }
}
```````````````| *(add output screenshot here)* |

---

### Assignment 14

**Student Registration Form using Java Swing and JDBC — stores student data in a MySQL database.**

> **Note:** Requires MySQL JDBC Driver (`mysql-connector-java.jar`) in NetBeans project libraries.  
> Create DB first: `CREATE DATABASE college; USE college;`  
> `CREATE TABLE students(id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(50), roll VARCHAR(20), branch VARCHAR(30), email VARCHAR(50));`

| Code | Output |
| --- | --- |
| ```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.sql.*;

public class StudentRegistration extends JFrame {
    JTextField nameField   = new JTextField(20);
    JTextField rollField   = new JTextField(20);
    JTextField branchField = new JTextField(20);
    JTextField emailField  = new JTextField(20);
    JLabel statusLabel     = new JLabel(" ");

    StudentRegistration() {
        setTitle("Student Registration");
        setSize(400, 300);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setLayout(new GridLayout(6, 2, 5, 5));

        add(new JLabel("Name:"));    add(nameField);
        add(new JLabel("Roll No:")); add(rollField);
        add(new JLabel("Branch:"));  add(branchField);
        add(new JLabel("Email:"));   add(emailField);

        JButton submit = new JButton("Register");
        submit.addActionListener(e -> saveToDatabase());
        add(submit); add(statusLabel);

        setVisible(true);
    }

    void saveToDatabase() {
        String url  = "jdbc:mysql://localhost:3306/college";
        String user = "root";
        String pass = "";   // change to your password
        try (Connection con = DriverManager.getConnection(url, user, pass)) {
            String sql = "INSERT INTO students(name, roll, branch, email) VALUES(?,?,?,?)";
            PreparedStatement ps = con.prepareStatement(sql);
            ps.setString(1, nameField.getText());
            ps.setString(2, rollField.getText());
            ps.setString(3, branchField.getText());
            ps.setString(4, emailField.getText());
            ps.executeUpdate();
            statusLabel.setText("Registered successfully!");
        } catch (SQLException ex) {
            statusLabel.setText("DB Error: " + ex.getMessage());
        }
    }

    public static void main(String[] args) {
        new StudentRegistration();
    }
}
``````````````| *(add output screenshot here)* |

---

### Assignment 15

**JFrame with 10 buttons — each button performs a different functionality.**

| Code | Output |
| --- | --- |
| ```java
import javax.swing.*;
import java.awt.*;

public class TenButtons extends JFrame {

    TenButtons() {
        setTitle("10 Buttons Demo");
        setSize(500, 400);
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setLayout(new GridLayout(5, 2, 10, 10));

        JButton b1 = new JButton("1. Show Message");
        b1.addActionListener(e -> JOptionPane.showMessageDialog(this, "Hello from Button 1!"));

        JButton b2 = new JButton("2. Date & Time");
        b2.addActionListener(e -> JOptionPane.showMessageDialog(this, new java.util.Date().toString()));

        JButton b3 = new JButton("3. Random Number");
        b3.addActionListener(e -> JOptionPane.showMessageDialog(this, "Random: " + (int)(Math.random()*100)));

        JButton b4 = new JButton("4. Change BG Color");
        b4.addActionListener(e -> getContentPane().setBackground(
            new Color((int)(Math.random()*255),(int)(Math.random()*255),(int)(Math.random()*255))));

        JButton b5 = new JButton("5. Count Characters");
        b5.addActionListener(e -> {
            String input = JOptionPane.showInputDialog("Enter a string:");
            if (input != null) JOptionPane.showMessageDialog(this, "Length: " + input.length());
        });

        JButton b6 = new JButton("6. Reverse String");
        b6.addActionListener(e -> {
            String input = JOptionPane.showInputDialog("Enter a string:");
            if (input != null)
                JOptionPane.showMessageDialog(this, new StringBuilder(input).reverse().toString());
        });

        JButton b7 = new JButton("7. Even / Odd");
        b7.addActionListener(e -> {
            String input = JOptionPane.showInputDialog("Enter a number:");
            if (input != null) {
                int n = Integer.parseInt(input);
                JOptionPane.showMessageDialog(this, n + " is " + (n%2==0 ? "Even" : "Odd"));
            }
        });

        JButton b8 = new JButton("8. Quick Calc");
        b8.addActionListener(e -> {
            double a = Double.parseDouble(JOptionPane.showInputDialog("Enter num 1:"));
            double b2 = Double.parseDouble(JOptionPane.showInputDialog("Enter num 2:"));
            JOptionPane.showMessageDialog(this, "Sum=" + (a+b2) + "  Product=" + (a*b2));
        });

        JButton b9 = new JButton("9. Exit");
        b9.addActionListener(e -> {
            int res = JOptionPane.showConfirmDialog(this, "Exit?");
            if (res == JOptionPane.YES_OPTION) System.exit(0);
        });

        JButton b10 = new JButton("10. About");
        b10.addActionListener(e -> JOptionPane.showMessageDialog(this,
            "Java Swing Demo\nProgram 15\nNetBeans"));

        add(b1); add(b2); add(b3); add(b4); add(b5);
        add(b6); add(b7); add(b8); add(b9); add(b10);
        setVisible(true);
    }

    public static void main(String[] args) {
        new TenButtons();
    }
}
`````````````| *(add output screenshot here)* |

---

### Assignment 16

**Create three classes (A, B, C) — each with a method that prints 1 to 100 along with the class name.**

| Code | Output |
| --- | --- |
| ```java
class ClassA {
    public void printNumbers() {
        for (int i = 1; i <= 100; i++)
            System.out.println("ClassA: " + i);
    }
}

class ClassB {
    public void printNumbers() {
        for (int i = 1; i <= 100; i++)
            System.out.println("ClassB: " + i);
    }
}

class ClassC {
    public void printNumbers() {
        for (int i = 1; i <= 100; i++)
            System.out.println("ClassC: " + i);
    }
}

public class MultiClassPrint {
    public static void main(String[] args) {
        new ClassA().printNumbers();
        new ClassB().printNumbers();
        new ClassC().printNumbers();
    }
}
````````````| *(add output screenshot here)* |

---

### Assignment 17

**Three classes printing 1 to 10 sequentially — without using threads.**

| Code | Output |
| --- | --- |
| ```java
class PrinterX {
    public void print() {
        System.out.println("\n--- PrinterX ---");
        for (int i = 1; i <= 10; i++)
            System.out.println("PrinterX: " + i);
    }
}

class PrinterY {
    public void print() {
        System.out.println("\n--- PrinterY ---");
        for (int i = 1; i <= 10; i++)
            System.out.println("PrinterY: " + i);
    }
}

class PrinterZ {
    public void print() {
        System.out.println("\n--- PrinterZ ---");
        for (int i = 1; i <= 10; i++)
            System.out.println("PrinterZ: " + i);
    }
}

public class SequentialPrint {
    public static void main(String[] args) {
        System.out.println("Running without threads - strictly sequential:");
        new PrinterX().print();
        new PrinterY().print();
        new PrinterZ().print();
        System.out.println("\nAll done. Output is always in order (X -> Y -> Z).");
    }
}
```````````| *(add output screenshot here)* |

---

### Assignment 18

**Three classes printing 1 to 10 using the Runnable interface.**

| Code | Output |
| --- | --- |
| ```java
class RunnableX implements Runnable {
    public void run() {
        for (int i = 1; i <= 10; i++) {
            System.out.println("RunnableX: " + i);
            try { Thread.sleep(10); } catch (InterruptedException e) {}
        }
    }
}

class RunnableY implements Runnable {
    public void run() {
        for (int i = 1; i <= 10; i++) {
            System.out.println("RunnableY: " + i);
            try { Thread.sleep(10); } catch (InterruptedException e) {}
        }
    }
}

class RunnableZ implements Runnable {
    public void run() {
        for (int i = 1; i <= 10; i++) {
            System.out.println("RunnableZ: " + i);
            try { Thread.sleep(10); } catch (InterruptedException e) {}
        }
    }
}

public class RunnableDemo {
    public static void main(String[] args) throws InterruptedException {
        Thread t1 = new Thread(new RunnableX());
        Thread t2 = new Thread(new RunnableY());
        Thread t3 = new Thread(new RunnableZ());

        t1.start(); t2.start(); t3.start();

        t1.join(); t2.join(); t3.join();
        System.out.println("All threads finished!");
    }
}
``````````| *(add output screenshot here)* |

---

### Assignment 19

**File copy using both Byte Stream and Character Stream.**

| Code | Output |
| --- | --- |
| ```java
import java.io.*;

public class FileCopy {

    public static void copyByteStream(String src, String dest) {
        try (FileInputStream fis = new FileInputStream(src);
             FileOutputStream fos = new FileOutputStream(dest)) {
            byte[] buffer = new byte[1024];
            int bytesRead;
            while ((bytesRead = fis.read(buffer)) != -1)
                fos.write(buffer, 0, bytesRead);
            System.out.println("Byte Stream copy done: " + dest);
        } catch (IOException e) {
            System.out.println("Error (Byte Stream): " + e.getMessage());
        }
    }

    public static void copyCharStream(String src, String dest) {
        try (FileReader fr = new FileReader(src);
             FileWriter fw = new FileWriter(dest)) {
            char[] buffer = new char[1024];
            int charsRead;
            while ((charsRead = fr.read(buffer)) != -1)
                fw.write(buffer, 0, charsRead);
            System.out.println("Character Stream copy done: " + dest);
        } catch (IOException e) {
            System.out.println("Error (Char Stream): " + e.getMessage());
        }
    }

    public static void main(String[] args) throws IOException {
        try (FileWriter fw = new FileWriter("source.txt")) {
            fw.write("Hello, this is test content for file copy demonstration!\n");
            fw.write("Java file I/O is simple and powerful.");
        }

        copyByteStream("source.txt", "copy_byte.txt");
        copyCharStream("source.txt", "copy_char.txt");
    }
}
`````````| *(add output screenshot here)* |

---

### Assignment 20

**ArrayList operations — add, remove, search, update, and iteration.**

| Code | Output |
| --- | --- |
| ```java
import java.util.ArrayList;
import java.util.Iterator;

public class ArrayListDemo {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();

        list.add("Apple"); list.add("Banana"); list.add("Cherry");
        list.add("Date");  list.add("Elderberry");
        System.out.println("After adding: " + list);

        list.remove("Date");
        System.out.println("After removing 'Date': " + list);

        System.out.println("Contains 'Cherry': " + list.contains("Cherry"));
        System.out.println("Index of 'Banana': " + list.indexOf("Banana"));

        list.set(1, "Blueberry");
        System.out.println("After updating index 1: " + list);

        System.out.print("Iterating: ");
        Iterator<String> it = list.iterator();
        while (it.hasNext()) System.out.print(it.next() + " ");
        System.out.println();

        System.out.println("Size: " + list.size());
    }
}
````````| *(add output screenshot here)* |

---

### Assignment 21

**LinkedList operations — insert at beginning, middle, and end; delete; search; display.**

| Code | Output |
| --- | --- |
| ```java
import java.util.LinkedList;
import java.util.ListIterator;

public class LinkedListDemo {
    public static void main(String[] args) {
        LinkedList<Integer> list = new LinkedList<>();

        list.add(10); list.add(20); list.add(40); list.add(50);
        System.out.println("Initial: " + list);

        list.addFirst(5);
        System.out.println("After addFirst(5): " + list);

        list.add(3, 30);
        System.out.println("After add(3, 30): " + list);

        list.addLast(60);
        System.out.println("After addLast(60): " + list);

        list.removeFirst();
        list.removeLast();
        System.out.println("After removing first & last: " + list);

        System.out.println("Contains 30: " + list.contains(30));
        System.out.println("Index of 30: " + list.indexOf(30));

        System.out.print("Forward traversal: ");
        ListIterator<Integer> it = list.listIterator();
        while (it.hasNext()) System.out.print(it.next() + " ");
        System.out.println();
    }
}
```````| *(add output screenshot here)* |

---

### Assignment 22

**Stack operations using Java Collections Framework — push, pop, peek, isEmpty, and search.**

| Code | Output |
| --- | --- |
| ```java
import java.util.Stack;

public class StackDemo {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        System.out.println("Is empty: " + stack.isEmpty());

        stack.push(10); stack.push(20); stack.push(30);
        stack.push(40); stack.push(50);
        System.out.println("After push: " + stack);

        System.out.println("Peek (top): " + stack.peek());

        System.out.println("Pop: " + stack.pop());
        System.out.println("After pop: " + stack);

        System.out.println("Search 20 (position from top): " + stack.search(20));

        System.out.println("Is empty: " + stack.isEmpty());

        while (!stack.isEmpty())
            System.out.print("Popped: " + stack.pop() + "  ");
        System.out.println("\nStack is now empty: " + stack.isEmpty());
    }
}
``````| *(add output screenshot here)* |

---

### Assignment 23

**HashMap operations — insert, retrieve, remove, and iterate key-value pairs.**

| Code | Output |
| --- | --- |
| ```java
import java.util.HashMap;
import java.util.Map;

public class HashMapDemo {
    public static void main(String[] args) {
        HashMap<Integer, String> map = new HashMap<>();

        map.put(1, "Alice");
        map.put(2, "Bob");
        map.put(3, "Charlie");
        map.put(4, "Diana");
        System.out.println("HashMap: " + map);

        System.out.println("Key 2 -> " + map.get(2));

        System.out.println("Contains key 3: " + map.containsKey(3));
        System.out.println("Contains value 'Bob': " + map.containsValue("Bob"));

        map.remove(1);
        System.out.println("After removing key 1: " + map);

        System.out.println("Iterating:");
        for (Map.Entry<Integer, String> entry : map.entrySet())
            System.out.println("  " + entry.getKey() + " => " + entry.getValue());

        System.out.println("Size: " + map.size());
    }
}
`````| *(add output screenshot here)* |

---

### Assignment 24

**TreeMap operations — insert, display in sorted order, search, and remove.**

| Code | Output |
| --- | --- |
| ```java
import java.util.TreeMap;
import java.util.Map;

public class TreeMapDemo {
    public static void main(String[] args) {
        TreeMap<Integer, String> tmap = new TreeMap<>();

        tmap.put(5, "Eve");
        tmap.put(2, "Bob");
        tmap.put(8, "Henry");
        tmap.put(1, "Alice");
        tmap.put(4, "Diana");

        System.out.println("TreeMap (sorted): " + tmap);

        System.out.println("First key: " + tmap.firstKey());
        System.out.println("Last key:  " + tmap.lastKey());

        System.out.println("Contains key 4: " + tmap.containsKey(4));
        System.out.println("Value at key 2: " + tmap.get(2));

        tmap.remove(5);
        System.out.println("After removing key 5: " + tmap);

        System.out.println("Iterate:");
        for (Map.Entry<Integer, String> e : tmap.entrySet())
            System.out.println("  " + e.getKey() + " -> " + e.getValue());
    }
}
````| *(add output screenshot here)* |

---

### Assignment 25

**Stack implementation using arrays — push, pop, peek, display, with overflow and underflow handling.**

| Code | Output |
| --- | --- |
| ```java
public class ArrayStack {
    int[] stack;
    int top;
    int maxSize;

    ArrayStack(int size) {
        maxSize = size;
        stack = new int[maxSize];
        top = -1;
    }

    public void push(int val) {
        if (top == maxSize - 1) {
            System.out.println("Stack OVERFLOW! Cannot push " + val);
            return;
        }
        stack[++top] = val;
        System.out.println("Pushed: " + val);
    }

    public int pop() {
        if (top == -1) {
            System.out.println("Stack UNDERFLOW! Stack is empty.");
            return -1;
        }
        return stack[top--];
    }

    public int peek() {
        if (top == -1) { System.out.println("Stack is empty."); return -1; }
        return stack[top];
    }

    public boolean isEmpty() { return top == -1; }

    public void display() {
        if (top == -1) { System.out.println("Stack is empty."); return; }
        System.out.print("Stack (top to bottom): ");
        for (int i = top; i >= 0; i--) System.out.print(stack[i] + " ");
        System.out.println();
    }

    public static void main(String[] args) {
        ArrayStack s = new ArrayStack(5);

        s.push(10); s.push(20); s.push(30); s.push(40); s.push(50);
        s.push(60);   // Overflow test
        s.display();
        System.out.println("Peek: " + s.peek());
        System.out.println("Pop: " + s.pop());
        s.display();

        s.pop(); s.pop(); s.pop(); s.pop();
        s.pop();  // Underflow test
        System.out.println("Is Empty: " + s.isEmpty());
    }
}
``` | *(add output screenshot here)* |

---

## 👩‍💻 Author

**Samiksha Rana**  
B.Tech — AI & Data Science, Mody University of Science & Technology  
🔗 [github.com/smiiksha](https://github.com/smiiksha)

---

> *Repository maintained as part of academic coursework. New assignments added progressively.*
