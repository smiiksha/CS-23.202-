# ☕ CS-23.202 — Java Laboratory
### B.Tech 2nd Year | Mody University of Science & Technology

![Java](https://img.shields.io/badge/Language-Java-orange?style=flat-square&logo=java)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat-square)
![Course](https://img.shields.io/badge/Course-CS--23.202-blue?style=flat-square)

---

## 📋 About

This repository contains all lab assignments for the **Java Programming Laboratory (CS-23.202)** course, 2nd Year B.Tech, AI & Data Science — Mody University of Science & Technology. Each program demonstrates core Object-Oriented Programming concepts in Java.

---

## 📂 Assignment Index

| # | Title |
|---|-------|
| [01](#assignment-1) | Write a class with four methods add, subtract, multiply and divide and test all the methods in the main |
| [02](#assignment-2) | Write a class for addition of two distances where each distance is given in mm, cm, m |
| [03](#assignment-3) | Write a class for addition of two times where each time is given in hr, min, sec |
| [04](#assignment-4) | Write a class for addition of two distances where each distance is given in m and cm |
| [05](#assignment-5) | Write a class for addition of two times where each time is given in hr and min |
| [06](#assignment-6) | Write a class to reverse a 1D array |
| [07](#assignment-7) | Write a class with necessary number of methods for matrix operations |
| [08](#assignment-8) | Collect all 5 codes of C language and convert them into object oriented Java |
| [09](#assignment-9) | Classes A, B, C printing 1–100 sequentially |
| [10](#assignment-10) | Multithreading with Thread classes X, Y, Z |
| [11](#assignment-11) | Multithreading using Runnable interface (Alpha, Beta, Gamma) |
| [12–14](#assignments-12-14) | Coming Soon |

---

## 💻 Assignments

---

### Assignment 1
**Write a class with four methods add, subtract, multiply and divide and test all the methods in the main.**

| Code | Output |
|------|--------|
| <pre>import java.util.Scanner;<br><br>class Operation {<br><br>    int a,b;<br><br>    void input(){<br>        Scanner s = new Scanner(System.in);<br>        System.out.println("Enter first number");<br>        a = s.nextInt();<br>        System.out.println("Enter second number");<br>        b = s.nextInt();<br>    }<br>    void add(){<br>        System.out.println("Addition = " + (a+b));<br>    }<br>    void sub(){<br>        System.out.println("Subtraction = " + (a-b));<br>    }<br>    void mul(){<br>        System.out.println("Multiplication = " + (a*b));<br>    }<br>    void div(){<br>        System.out.println("Division = " + (a/b));<br>    }<br>}<br>public class Calculator {<br>    public static void main(String[] args) {<br>        Operation obj = new Operation();<br>        obj.input();<br>        obj.add();<br>        obj.sub();<br>        obj.mul();<br>        obj.div();<br>    }<br>}</pre> | ![output](https://github.com/user-attachments/assets/cab2040d-0b33-41b4-87d9-8492f3bb6381) |

---

### Assignment 2
**Write a class for addition of two distances where each distance is given in mm, cm, m.**

| Code | Output |
|------|--------|
| <pre>import java.util.Scanner;<br>public class Distance {<br>    public static void main(String[]args){<br>        Test t1=new Test();<br>        Test t2=new Test();<br>        Test result=new Test();<br>        t1.input();<br>        t2.input();<br>        result.add(t1, t2);<br>        result.output();<br>    }<br>}<br><br>class Test{<br>    int m;<br>    int cm;<br>    int mm;<br>    void input(){<br>        Scanner s1=new Scanner(System.in);<br>        System.out.println("enter distance in m");<br>        m=s1.nextInt();<br>        Scanner s2=new Scanner(System.in);<br>        System.out.println("enter distance in cm");<br>        cm=s2.nextInt();<br>        Scanner s3=new Scanner(System.in);<br>        System.out.println("enter distance in mm");<br>        mm=s3.nextInt();<br>    }<br>    void output(){<br>        System.out.println("Distance in m"+m);<br>        System.out.println("Distance in cm"+cm);<br>        System.out.println("Distance in mm"+mm);<br>    }<br>    void add(Test d1,Test d2){<br>        m=d1.m+d2.m;<br>        cm=d1.cm+d2.cm;<br>        mm=d1.mm+d2.mm;<br>        if(mm>=10){<br>            cm=cm+1;<br>            mm=mm-10;<br>        }<br>        if(cm>=100){<br>            m=m+1;<br>            cm=cm-100;<br>        }<br>    }<br>}</pre> | ![output](https://github.com/user-attachments/assets/56844e6f-4fb8-4c69-8882-4e21493814c1) |

---

### Assignment 3
**Write a class for addition of two times where each time is given in hr, min, sec.**

| Code | Output |
|------|--------|
| <pre>import java.util.Scanner;<br><br>public class TimeHMS {<br>    public static void main(String[] args){<br>        TRY t1 = new TRY();<br>        TRY t2 = new TRY();<br>        TRY result = new TRY();<br>        t1.input();<br>        t2.input();<br>        result.add(t1,t2);<br>        result.output();<br>    }<br>}<br><br>class TRY{<br>    int hr,min,sec;<br>    void input(){<br>        Scanner s = new Scanner(System.in);<br>        System.out.println("Enter hours");<br>        hr = s.nextInt();<br>        System.out.println("Enter minutes");<br>        min = s.nextInt();<br>        System.out.println("Enter seconds");<br>        sec = s.nextInt();<br>    }<br>    void output(){<br>        System.out.println(hr+" hr "+min+" min "+sec+" sec");<br>    }<br>    void add(TRY t1,TRY t2){<br>        sec = t1.sec + t2.sec;<br>        min = t1.min + t2.min;<br>        hr = t1.hr + t2.hr;<br>        if(sec>=60){<br>            min = min + 1;<br>            sec = sec - 60;<br>        }<br>        if(min>=60){<br>            hr = hr + 1;<br>            min = min - 60;<br>        }<br>    }<br>}</pre> | ![output](https://github.com/user-attachments/assets/f3a5fd3f-af8c-4f3e-8cbc-2e5425c079f9) |

---

### Assignment 4
**Write a class for addition of two distances where each distance is given in m and cm.**

| Code | Output |
|------|--------|
| <pre>import java.util.Scanner;<br><br>public class DistanceMC {<br>    public static void main(String[] args){<br>        T d1 = new T();<br>        T d2 = new T();<br>        T result = new T();<br>        d1.input();<br>        d2.input();<br>        result.add(d1,d2);<br>        result.output();<br>    }<br>}<br><br>class T{<br>    int m,cm;<br>    void input(){<br>        Scanner s = new Scanner(System.in);<br>        System.out.println("Enter meter");<br>        m = s.nextInt();<br>        System.out.println("Enter centimeter");<br>        cm = s.nextInt();<br>    }<br>    void output(){<br>        System.out.println("Meter = "+m);<br>        System.out.println("Centimeter = "+cm);<br>    }<br>    void add(T d1,T d2){<br>        cm = d1.cm + d2.cm;<br>        m = d1.m + d2.m;<br>        if(cm>=100){<br>            m = m + 1;<br>            cm = cm - 100;<br>        }<br>    }<br>}</pre> | ![output](https://github.com/user-attachments/assets/03271c3d-f033-431d-81eb-ffff622641cc) |

---

### Assignment 5
**Write a class for addition of two times where each time is given in hr and min.**

| Code | Output |
|------|--------|
| <pre>import java.util.Scanner;<br><br>public class TimeHM {<br>    public static void main(String[] args){<br>        Tt t1 = new Tt();<br>        Tt t2 = new Tt();<br>        Tt result = new Tt();<br>        t1.input();<br>        t2.input();<br>        result.add(t1,t2);<br>        result.output();<br>    }<br>}<br><br>class Tt{<br>    int hr,min;<br>    void input(){<br>        Scanner s = new Scanner(System.in);<br>        System.out.println("Enter hours");<br>        hr = s.nextInt();<br>        System.out.println("Enter minutes");<br>        min = s.nextInt();<br>    }<br>    void output(){<br>        System.out.println(hr+" hr "+min+" min");<br>    }<br>    void add(Tt t1,Tt t2){<br>        min = t1.min + t2.min;<br>        hr = t1.hr + t2.hr;<br>        if(min>=60){<br>            hr = hr + 1;<br>            min = min - 60;<br>        }<br>    }<br>}</pre> | ![output](https://github.com/user-attachments/assets/8cadc746-890a-4eb2-970f-8ae99b089335) |

---

### Assignment 6
**Write a class to reverse a 1D array. Also includes C-to-Java conversion programs: Factorial, Palindrome, Armstrong, Prime.**

| Code | Output |
|------|--------|
| <pre>import java.util.Scanner;<br><br>public class PalindromeNumber {<br>    public static void main(String[] args){<br>        Scanner sc=new Scanner(System.in);<br>        int num,original,reverse=0,remainder;<br>        System.out.println("enter a number:");<br>        num=sc.nextInt();<br>        original=num;<br>        while (num!=0){<br>            remainder=num%10;<br>            reverse=reverse*10+remainder;<br>            num=num/10;<br>        }<br>        if(original==reverse){<br>            System.out.println("number is palindrome");<br>        }<br>        else{<br>            System.out.println("number is not palindrome");<br>        }<br>    }<br>}<br><br>public class NumberPrograms {<br>    public static void main(String[] args){<br>        Tt3 t = new Tt3();<br>        t.input();<br>        t.factorial();<br>        t.palindrome();<br>        t.armstrong();<br>        t.prime();<br>    }<br>}<br><br>class Tt3{<br>    int n;<br>    void input(){<br>        Scanner s = new Scanner(System.in);<br>        System.out.println("Enter number");<br>        n = s.nextInt();<br>    }<br>    void factorial(){<br>        int fact = 1;<br>        for(int i=1;i<=n;i++){<br>            fact = fact * i;<br>        }<br>        System.out.println("Factorial = "+fact);<br>    }<br>    void palindrome(){<br>        int temp = n;<br>        int rev = 0;<br>        while(temp>0){<br>            rev = rev*10 + temp%10;<br>            temp = temp/10;<br>        }<br>        if(rev==n)<br>            System.out.println("Palindrome");<br>        else<br>            System.out.println("Not Palindrome");<br>    }<br>    void armstrong(){<br>        int temp = n;<br>        int sum = 0;<br>        while(temp>0){<br>            int d = temp%10;<br>            sum = sum + d*d*d;<br>            temp = temp/10;<br>        }<br>        if(sum==n)<br>            System.out.println("Armstrong");<br>        else<br>            System.out.println("Not Armstrong");<br>    }<br>    void prime(){<br>        int flag = 0;<br>        for(int i=2;i<n;i++){<br>            if(n%i==0){<br>                flag = 1;<br>                break;<br>            }<br>        }<br>        if(flag==0)<br>            System.out.println("Prime");<br>        else<br>            System.out.println("Not Prime");<br>    }<br>}</pre> | ![output](https://github.com/user-attachments/assets/5dca7759-364b-4160-b884-603e963411e2) |

---

### Assignment 7
**Write a class with necessary number of methods for matrix operations: transpose, addition, multiplication, sum of two rows, sum of columns and sum of diagonals of the matrix.**

> *Coming soon — code will be added here.*

---

### Assignment 8
**Collect all 5 codes of C language like factorial, armstrong, palindrome etc and convert them into object oriented in Java and test the result in main.**

> *See Assignment 6 for reference implementation.*

---

### Assignment 9
**Create three classes A, B, C — each with a fun() method that prints its label from 1 to 100. Call them sequentially from main.**

| Code | Output |
|------|--------|
| <pre>package com.mycompany.samikshac2;<br><br>// Class A<br>class A {<br>    void fun() {<br>        for (int i = 1; i <= 100; i++) {<br>            System.out.println("a" + i);<br>        }<br>    }<br>}<br><br>// Class B<br>class B {<br>    void fun() {<br>        for (int i = 1; i <= 100; i++) {<br>            System.out.println("b" + i);<br>        }<br>    }<br>}<br><br>// Class C<br>class C {<br>    void fun() {<br>        for (int i = 1; i <= 100; i++) {<br>            System.out.println("c" + i);<br>        }<br>    }<br>}<br><br>// Main class<br>public class main {<br>    public static void main(String[] args) {<br>        A objA = new A();<br>        B objB = new B();<br>        C objC = new C();<br>        objA.fun();<br>        objB.fun();<br>        objC.fun();<br>    }<br>}</pre> | ![output1](https://github.com/user-attachments/assets/f4e6a370-7798-4d19-8742-c84a52e80964) ![output2](https://github.com/user-attachments/assets/aa8fde25-bae7-46c6-a35e-a50dfb1d20d0) ![output3](https://github.com/user-attachments/assets/725d725a-49b3-4d3d-9d14-3dc8a28fe5cb) ![output4](https://github.com/user-attachments/assets/6d1b379a-0a95-4b2a-b576-654fd3c31a79) ![output5](https://github.com/user-attachments/assets/96337d58-3837-4879-9862-a3a9bf1a3493) ![output6](https://github.com/user-attachments/assets/6fbd8154-6342-4080-ac91-86b072cf2bbb) ![output7](https://github.com/user-attachments/assets/c1dcede9-7669-493f-8a49-9d789901290f) ![output8](https://github.com/user-attachments/assets/e0b9ba29-f7e1-4e82-adba-1a650ea99a9d) ![output9](https://github.com/user-attachments/assets/9892582e-0efa-42cc-8878-38dd8f94bbf8) |

---

### Assignment 10
**Create three thread classes X, Y, Z — each prints its label 1 to 100 with a sleep of 100ms. Stop thread X after 1 second from main.**

| Code | Output |
|------|--------|
| <pre>package com.mycompany.samikshac2;<br><br>// Thread class X<br>class X extends Thread {<br>    public void run() {<br>        for(int i = 1; i <= 100; i++) {<br>            System.out.println("x" + i);<br>            try {<br>                sleep(100);<br>            } catch(Exception e) {}<br>        }<br>    }<br>}<br><br>class Y extends Thread {<br>    public void run() {<br>        for(int i = 1; i <= 100; i++) {<br>            System.out.println("y" + i);<br>            try {<br>                sleep(100);<br>            } catch(Exception e) {}<br>        }<br>    }<br>}<br><br>class Z extends Thread {<br>    public void run() {<br>        for(int i = 1; i <= 100; i++) {<br>            System.out.println("z" + i);<br>            try {<br>                sleep(100);<br>            } catch(Exception e) {}<br>        }<br>    }<br>}<br><br>public class ThreadMain {<br>    public static void main(String[] args) {<br>        X t1 = new X();<br>        Y t2 = new Y();<br>        Z t3 = new Z();<br>        t1.start();<br>        t2.start();<br>        t3.start();<br>        try {<br>            Thread.sleep(1000);<br>            t1.stop();<br>        } catch(Exception e) {}<br>    }<br>}</pre> | ![output1](https://github.com/user-attachments/assets/ac55c702-d9db-4450-a3b9-f38f9919cbd3) ![output2](https://github.com/user-attachments/assets/76319b40-e4d6-4bc4-ba64-b2613a2e8782) ![output3](https://github.com/user-attachments/assets/d5414ef8-383b-4c61-aa37-61c0bc2084a9) ![output4](https://github.com/user-attachments/assets/595886b6-6e8a-4583-9a9e-c7940326045f) ![output5](https://github.com/user-attachments/assets/f81a0a1c-664d-43fb-94c5-c646c6d5fd4a) ![output6](https://github.com/user-attachments/assets/2d5ca806-cc1a-42ca-a9f1-e03ce7a57398) ![output7](https://github.com/user-attachments/assets/2eaee1a3-2c7f-4184-aa54-40857be7e261) ![output8](https://github.com/user-attachments/assets/ce8ccd56-4145-42fd-9c6b-d56b91aa2fcc) ![output9](https://github.com/user-attachments/assets/89bb7854-1fac-455f-891a-7020959d9a60) ![output10](https://github.com/user-attachments/assets/a8d5ffd1-2275-4114-8073-d224e1e47e6a) |

---

### Assignment 11
**Implement multithreading using the Runnable interface with three classes: Alpha, Beta, Gamma — each printing 1 to 100. Stop Alpha thread after 500ms.**

| Code | Output |
|------|--------|
| <pre>package com.mycompany.samikshac2;<br><br>class Alpha implements Runnable {<br>    public void run() {<br>        for(int i = 1; i <= 100; i++) {<br>            System.out.println("alpha" + i);<br>            try {<br>                Thread.sleep(50);<br>            } catch(Exception e) {}<br>        }<br>    }<br>}<br><br>class Beta implements Runnable {<br>    public void run() {<br>        for(int i = 1; i <= 100; i++) {<br>            System.out.println("beta" + i);<br>            try {<br>                Thread.sleep(50);<br>            } catch(Exception e) {}<br>        }<br>    }<br>}<br><br>class Gamma implements Runnable {<br>    public void run() {<br>        for(int i = 1; i <= 100; i++) {<br>            System.out.println("gamma" + i);<br>            try {<br>                Thread.sleep(50);<br>            } catch(Exception e) {}<br>        }<br>    }<br>}<br><br>public class RunnableProgram {<br>    public static void main(String[] args) {<br>        Alpha a = new Alpha();<br>        Beta b = new Beta();<br>        Gamma c = new Gamma();<br>        Thread t1 = new Thread(a);<br>        Thread t2 = new Thread(b);<br>        Thread t3 = new Thread(c);<br>        t1.start();<br>        t2.start();<br>        t3.start();<br>        try {<br>            Thread.sleep(500);<br>            t1.stop();<br>        } catch(Exception e) {}<br>    }<br>}</pre> | ![output1](https://github.com/user-attachments/assets/fa25dead-0488-4adf-8240-fc6baf420d4c) ![output2](https://github.com/user-attachments/assets/3896cbc3-9651-4a85-8a16-4032bc772715) ![output3](https://github.com/user-attachments/assets/cdf76977-7d23-49dd-92fd-6bf0694edc61) ![output4](https://github.com/user-attachments/assets/ae455223-b9ab-45a6-ab2e-15f1b01a4410) ![output5](https://github.com/user-attachments/assets/dd6294c8-112a-4f63-b238-c9b2f16c57b2) ![output6](https://github.com/user-attachments/assets/610f64e0-b77d-4d70-a1d5-40acea615cba) ![output7](https://github.com/user-attachments/assets/01ca8c34-3a33-4508-928d-37f58ab27328) ![output8](https://github.com/user-attachments/assets/07faeaef-6a74-4940-8c55-8b5f4a824521) |

---

### Assignments 12–14
> *To be updated as new assignments are completed.*

---


## 👩‍💻 Author

**Samiksha Rana**  
B.Tech — AI & Data Science, Mody University of Science & Technology  
🔗 [github.com/smiiksha](https://github.com/smiiksha)

---

> *Repository maintained as part of academic coursework. New assignments added progressively.*
