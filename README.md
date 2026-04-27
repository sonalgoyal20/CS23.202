# CS-23.202 JAVA LABORATORY (2ND YEAR)

*INDEX*
[Program-1 Write a class with four methods add, subtract, multiply and divide and test all the methods in the main](#ASSIGNMENT-1)

[Program-2 Write a class for addition of two distances where each distance is given in m, cm and mm](#ASSIGNMENT-2)

[Program-3 Write a class for addition of two times where each time is given in hr, min and sec](#ASSIGNMENT-3)

[Program-4 Write a class for addition of two distances where each distance is given in m and cm](#ASSIGNMENT-4)

[Program-5 Write a class for addition of two times where each timee is given in hr and min](#ASSIGNMENT-5)

[Program-6 Write a class to reverse an 1D array with necessary methods](#ASSIGNMENT-6)

[Program-7 Write a class with necessary number of methods for number ppf matrix operations: Transpose, Addition, Multiplication, Sum of rows, Sum of columns and Sum of diagonals of the matrix](#ASSIGNMENT-7)

[Program-8 Collect any 5 codes in c language like factorial, armstrong, palindrome etc and convert them in object oriented in java and test the result in the main](#ASSIGNMENT-8)

[Program-9 Create a parent class and two child class having same method which override it in both child classes. Call the methods using a parent class reference.](#ASSIGNMENT-9)

[Program-10 Write a Java Swing program that creates a GUI with buttons to draw and fill shapes (rectangle, oval) and change their colors (red, black) using the Graphics class.](#ASSIGNMENT-10)

[Program-11 Write a Java Swing program to design a simple calculator GUI that takes two inputs and performs addition, subtraction, multiplication, and division, displaying the result in an output field.](#ASSIGNMENT-11)

[Program-12 Write a Java Swing program that allows freehand drawing with the mouse, where users can change the drawing color using buttons (red, black, blue, magenta) and adjust the brush size using a slider.](#Assignment-12)

[Program-13 Implement a Java class Division with methods for integer division, floating-point division, division with remainder, and dividing multiple numbers by a given divisor. Ensure division by zero is properly handled with exceptions.](#Assignment-13)

[Program-14 Create a Student Registration Form using Java and store the entered data in a database using JDBC (Java Database Connectivity).](#ASSIGNMENT-14)

[Program-15 Create a GUI using JFrame that contains 10 buttons, each with different functionalities or structure.](#ASSIGNMENT-15)

[Program-16 Write a Java program consisting of three classes, where each class contains a method. Each method should print numbers from 1 to 100 along with the class name.](#ASSIGNMENT-16)

[Program-17 Using three different classes and methods, write a Java program to print numbers from 1 to 100: With using threads analyze and display the result](#ASSIGNMENT-17)

[Prpgram-18 Repeat above program 17 using the Runnable interface.](#ASSIGNMENT-18)

[Program-19 Implement File transfer/copy in Java using: 1.Byte Stream 2.Character Stream](#ASSIGNMENT-19)

[Program-20 Write a Java program to demonstrate the use of ArrayList by performing operations such as adding elements, removing elements, searching for an element, updating elements, and iterating through the list.](#ASSIGNMENT-20)

[Program-21 Write a Java program to implement LinkedList and perform insertion at the beginning, middle, and end, along with deletion, searching, and displaying the elements.](#ASSIGNEMNT-21)

[Program-22 Write a Java program to demonstrate Stack operations using the Collection Framework, including push, pop, peek, and checking whether the stack is empty.](#ASSIGNMENT-22)

[Program-23 Write a Java program to implement HashMap and perform operations such as inserting key-value pairs, retrieving values using keys, removing entries, and iterating through the map.](#ASSIGNMENT-23)

[Program-24 Write a Java program to demonstrate TreeMap by inserting elements, displaying them in sorted order, searching for a key, and removing elements.](#ASSIGNMENT-24)

[Program-25 Write a Java program to implement a Stack using arrays and perform operations such as push, pop, displaying elements, and handling stack overflow and underflow conditions.](#ASSSIGNMENT-25)
## ASSIGNMENT-1
~~~
public class Calculator{

    public static void main(String[] args) {

        Calculatortest o1 = new Calculatortest();

        o1.add(10, 5);
        o1.subtract(10, 5);
        o1.multiply(10, 5);
        o1.divide(10, 5);
    }
}
class Calculatortest {

    // Addition
    void add(int a, int b) {
        System.out.println("Addition = " + (a + b));
    }

    // Subtraction
    void subtract(int a, int b) {
        System.out.println("Subtraction = " + (a - b));
    }

    // Multiplication
    void multiply(int a, int b) {
        System.out.println("Multiplication = " + (a * b));
    }

    // Division
    void divide(int a, int b) {
        System.out.println("Division = " + (a / b));
    }
}
~~~
<img width="1157" height="446" alt="Screenshot 2026-04-27 211826" src="https://github.com/user-attachments/assets/e9315be3-46e7-4777-873b-58e0ae269d94" />




## ASSIGNMENT-2
~~~
import java.util.Scanner;
public class DistanceTest {
     public static void main(String[] args) {
        Distance d1= new Distance();
        Distance d2= new Distance();
        Distance d3= new Distance();
        d1.input();
        d2.input();
        d3.add(d1,d2);
        d3.output();
    }
    
}
class Distance {
    int mtr;
    int cm;
    int mm;
    
    //method to take input
     void input(){
        Scanner sc = new Scanner(System.in);
         
         System.out.print("Enter metre:");
         mtr=sc.nextInt();
         
         System.out.print("Enter centimetre:");
         cm=sc.nextInt();
         
         System.out.print("Enter millimetre:");
         mm=sc.nextInt();
     }
     //Method to display output
     void output() {
         System.out.println("metre="+mtr);
         System.out.println("centimetre="+cm);
         System.out.println("millimetre="+mm);
     }
     void add(Distance d1, Distance d2) {
         mtr=d1.mtr+d2.mtr;
         cm=d1.cm+d2.cm;
         mm=d1.mm+d2.mm;
         if (mtr>=10)
         {
             mm=mm-10;
             cm=cm+1;
         }
         if (cm>=100)
         {
             cm=cm-100;
             mtr=mtr+1;
            
         }
     }
}
~~~
<img width="1242" height="665" alt="image" src="https://github.com/user-attachments/assets/fd8280ae-d0cc-4d25-8a4e-052e816f9341" />


## ASSIGNMENT-3
~~~
import java.util.Scanner;
public class Clocktest {
    public static void main(String[] args) {
        clock c1= new clock();
        clock c2= new clock();
        clock c3= new clock();
        c1.input();
        c2.input();
        c3.add(c1,c2);
        c3.output();
    }
    
}
class clock {
    int hr;
    int min;
    int sec;
    
    //method to take input
     void input(){
        Scanner sc = new Scanner(System.in);
         
         System.out.print("Enter hours:");
         hr=sc.nextInt();
         
         System.out.print("Enter minutes:");
         min=sc.nextInt();
         
         System.out.print("Enter seconds:");
         sec=sc.nextInt();
     }
     //Method to display output
     void output() {
         System.out.println("hours="+hr);
         System.out.println("minutes="+min);
         System.out.println("seconds="+sec);
     }
     void add(clock c1, clock c2) {
         hr=c1.hr+c2.hr;
         min=c1.min+c2.min;
         sec=c1.sec+c2.sec;
         if (sec>=60)
         {
             sec=sec-60;
             min=min+1;
         }
         if (min>=60)
         {
             min=min-60;
             hr=hr+1;
            
         }
     }
}
~~~
<img width="1247" height="648" alt="image" src="https://github.com/user-attachments/assets/7a62b4aa-9cb1-4b34-b795-12319cd3b133" />

## ASSIGNMENT-4
~~~
import java.util.Scanner;
public class Distancetest {
     public static void main(String[] args) {
        Distance d1= new Distance();
        Distance d2= new Distance();
        Distance d3= new Distance();
        d1.input();
        d2.input();
        d3.add(d1,d2);
        d3.output();
    }
    
}
class Distance {
    int mtr;
    int cm; 
    //method to take input
     void input(){
        Scanner sc = new Scanner(System.in);
         
         System.out.print("Enter metre:");
         mtr=sc.nextInt();
         
         System.out.print("Enter centimetre:");
         cm=sc.nextInt();
     }
     //Method to display output
     void output() {
         System.out.println("metre="+mtr);
         System.out.println("centimetre="+cm);
     }
     void add(Distance d1, Distance d2) {
         mtr=d1.mtr+d2.mtr;
         cm=d1.cm+d2.cm;
         if (cm>=100)
         {
             cm=cm-100;
             mtr=mtr+1;
            
         }
     }
}
~~~
<img width="1567" height="660" alt="Screenshot 2026-04-27 212334" src="https://github.com/user-attachments/assets/f32db087-683c-4482-a2ea-d5b5f62025f3" />


## ASSIGNMENT-5
~~~
import java.util.Scanner;
public class Clocktest {
    public static void main(String[] args) {
        clock c1= new clock();
        clock c2= new clock();
        clock c3= new clock();
        c1.input();
        c2.input();
        c3.add(c1,c2);
        c3.output();
    }
    
}
class clock {
    int hr;
    int min;
    
    //method to take input
     void input(){
        Scanner sc = new Scanner(System.in);
         
         System.out.print("Enter hours:");
         hr=sc.nextInt();
         
         System.out.print("Enter minutes:");
         min=sc.nextInt();
     }
     //Method to display output
     void output() {
         System.out.println("hours="+hr);
         System.out.println("minutes="+min);
     }
     void add(clock c1, clock c2) {
         hr=c1.hr+c2.hr;
         min=c1.min+c2.min;
         if (min>=60)
         {
             min=min-60;
             hr=hr+1;
            
         }
     }
}
~~~
<img width="1550" height="700" alt="Screenshot 2026-04-27 212624" src="https://github.com/user-attachments/assets/0899e10b-d7c9-4319-a9c3-036d00e64667" />



## ASSIGNMENT-6
~~~

import java.util.Scanner;
public class ArrayTest {
  public static void main(String[] args){  
      Array a= new Array();
      a.input();
      a.process();
      System.out.println("Entered Array:");
      a.outputarr();
      System.out.println("Reversed Array:");
      a.outputrev();
}
}
class Array{
    int arr[];
    int rev[];
    void input(){
        arr= new int[5];
        Scanner sc= new Scanner (System.in);
        for( int i=0;i<5;i++){
            System.out.println("Enter an element:");
            arr[i] = sc.nextInt();   
        }
    }
        void outputarr(){
        for(int i=0;i<5;i++){
            System.out.println(arr[i]);
    }
    }
        void outputrev(){
         for(int i=0;i<5;i++){
            System.out.println(rev[i]);    
        }
        }
       void process(){
            rev= new int[5];
            for (int i=0;i<5;i++){
                rev[4-i]=arr[i];
            }
        } 
}
~~~
<img width="1040" height="731" alt="Screenshot 2026-04-27 212722" src="https://github.com/user-attachments/assets/c7041c01-4068-4269-8d6f-41f6b79ee416" />


## ASSIGNMENT-7

~~~
import java.util.Scanner;

public class Matrixtest {

    public static void main(String[] args) {
        Matrix m1 = new Matrix();
        Matrix m2 = new Matrix();
        Matrix m3 = new Matrix();
        System.out.println("Enter First Matrix");
        m1.input();
        System.out.println("Enter Second Matrix");
        m2.input();
        System.out.println("Addition:");
        m3.add(m1, m2);
        m3.display();
        System.out.println("Multiplication:");
        m3.multiply(m1, m2);
        m3.display();
        m1.transpose();
        m1.sumRows();
        m1.sumColumns();
        m1.sumDiagonal();
    }
}

class Matrix {
   int a[][] = new int[3][3];

    // Input
    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the elements:");
        for (int i = 0; i < 3; i++)
            for (int j = 0; j < 3; j++)
                a[i][j] = sc.nextInt();
    }

    // Display
    void display() {
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++)
                System.out.print(a[i][j] + " ");
            System.out.println();
        }
    }

    // Addition
    void add(Matrix m1, Matrix m2) {
        for (int i = 0; i < 3; i++)
            for (int j = 0; j < 3; j++)
                a[i][j] = m1.a[i][j] + m2.a[i][j];
    }

    // Multiplication
    void multiply(Matrix m1, Matrix m2) {
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                a[i][j] = 0;
                for (int k = 0; k < 3; k++)
                    a[i][j] += m1.a[i][k] * m2.a[k][j];
            }
        }
    }

    // Transpose
    void transpose() {
        System.out.println("Transpose:");
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++)
                System.out.print(a[j][i] + " ");
            System.out.println();
        }
    }

    // Sum of rows
    void sumRows() {
        for (int i = 0; i < 3; i++) {
            int sum = 0;
            for (int j = 0; j < 3; j++)
                sum += a[i][j];
            System.out.println("Row " + i + " Sum = " + sum);
        }
    }

    // Sum of columns
    void sumColumns() {
        for (int j = 0; j < 3; j++) {
            int sum = 0;
            for (int i = 0; i < 3; i++)
                sum += a[i][j];
            System.out.println("Column " + j + " Sum = " + sum);
        }
    }

    // Diagonal sum
    void sumDiagonal() {
        int sum = 0;
        for (int i = 0; i < 3; i++)
            sum += a[i][i];

        System.out.println("Diagonal Sum = " + sum);
    }
}
~~~

<img width="757" height="803" alt="image" src="https://github.com/user-attachments/assets/6746ff5e-ffca-43bf-9ea3-9a7468d5d422" />

## ASSIGNMENT-8 
~~~
CODE IN C LANGUAGE:
#include<stdio.h>

// Factorial
void factorial(int n)
{
    int fact = 1;
    for(int i=1;i<=n;i++)
        fact = fact * i;

    printf("Factorial = %d\n", fact);
}

// Prime Number
void prime(int n)
{
    int count = 0;
    for(int i=1;i<=n;i++)
        if(n%i==0)
            count++;

    if(count==2)
        printf("Prime Number\n");
    else
        printf("Not Prime\n");
}

// Palindrome
void palindrome(int n)
{
    int temp=n, rev=0, r;

    while(n>0)
    {
        r=n%10;
        rev=rev*10+r;
        n=n/10;
    }

    if(temp==rev)
        printf("Palindrome Number\n");
    else
        printf("Not Palindrome\n");
}

// Swapping
void swap(int a,int b)
{
    int temp;

    printf("Before Swapping: a=%d b=%d\n",a,b);

    temp=a;
    a=b;
    b=temp;

    printf("After Swapping: a=%d b=%d\n",a,b);
}

// Star Pattern
void pattern(int n)
{
    printf("Star Pattern:\n");

    for(int i=1;i<=n;i++)
    {
        for(int j=1;j<=i;j++)
            printf("* ");
        printf("\n");
    }
}

int main()
{
    int n,a,b;

    printf("Enter number: ");
    scanf("%d",&n);

    factorial(n);
    prime(n);
    palindrome(n);

    printf("Enter two numbers for swapping: ");
    scanf("%d%d",&a,&b);

    swap(a,b);

    pattern(n);

    return 0;
}
CODE IN JAVA:
import java.util.Scanner;
public class CtoJAVA {
     public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        code obj = new code();

        System.out.print("Enter number: ");
        int n = sc.nextInt();

        obj.factorial(n);
        obj.prime(n);
        obj.palindrome(n);

        System.out.print("Enter two numbers for swapping: ");
        int a = sc.nextInt();
        int b = sc.nextInt();
        obj.swap(a, b);
        obj.pattern(n);    
}
}
class code {

    // Factorial
    void factorial(int n) {
        int fact = 1;
        for(int i = 1; i <= n; i++)
            fact *= i;
            System.out.println("Factorial = " + fact);
    }

    // Prime Number
    void prime(int n) {
        int count = 0;

        for(int i = 1; i <= n; i++)
            if(n % i == 0)
                count++;

        if(count == 2)
            System.out.println("Prime Number");
        else
            System.out.println("Not Prime");
    }

    // Palindrome Number
    void palindrome(int n) {
        int temp = n, rev = 0, r;

        while(n > 0) {
            r = n % 10;
            rev = rev * 10 + r;
            n /= 10;
        }

        if(temp == rev)
            System.out.println("Palindrome Number");
        else
            System.out.println("Not Palindrome");
    }

    // Swapping two numbers
    void swap(int a, int b) {
        System.out.println("Before Swapping: a=" + a + " b=" + b);

        int temp = a;
        a = b;
        b = temp;

        System.out.println("After Swapping: a=" + a + " b=" + b);
    }

    // Star Pattern
    void pattern(int n) {
        System.out.println("Star Pattern:");
        for(int i = 1; i <= n; i++) {
            for(int j = 1; j <= i; j++)
                System.out.print("* ");
            System.out.println();
        }
    }
}

~~~

<img width="1060" height="776" alt="image" src="https://github.com/user-attachments/assets/a702ecc9-2d3f-4c4f-b393-e541e93cae52" />

## ASSIGNMENT-9
~~~
class Parent {
    void show() {
        System.out.println("This is Parent class method");
    }
}

class Child1 extends Parent {
    void show() {
        System.out.println("This is Child1 class method");
    }
}

class Child2 extends Parent {
    void show() {
        System.out.println("This is Child2 class method");
    }
}

public class Program9 {
    public static void main(String[] args) {
        Parent obj;

        obj = new Child1();
        obj.show();

        obj = new Child2();
        obj.show();
    }
}
~~~

<img width="1041" height="388" alt="image" src="https://github.com/user-attachments/assets/7b5ca34e-7494-4e39-bb11-36798da691c6" />

## ASSIGNMENT-10
~~~
import java.awt.Color;
import java.awt.Graphics;

public class JFrame1 extends javax.swing.JFrame {
    String shape = "rect";
    Color color = Color.RED;
    /**
     * Creates new form JFrame1
     */
    public JFrame1() {
        initComponents();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jButton1 = new javax.swing.JButton();
        jButton2 = new javax.swing.JButton();
        jButton3 = new javax.swing.JButton();
        jButton4 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jButton1.setText("Rectangle");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        jButton2.setText("Oval");
        jButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton2ActionPerformed(evt);
            }
        });

        jButton3.setText("Red");
        jButton3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton3ActionPerformed(evt);
            }
        });

        jButton4.setText("Black");
        jButton4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton4ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(32, 32, 32)
                .addComponent(jButton1)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jButton2)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jButton3)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jButton4)
                .addContainerGap(51, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap(261, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton1)
                    .addComponent(jButton3)
                    .addComponent(jButton2)
                    .addComponent(jButton4))
                .addGap(16, 16, 16))
        );

        pack();
    }// </editor-fold>                        
 @Override
    public void paint(Graphics g) {
        super.paint(g);

        g.setColor(color);

        if (shape.equals("rect")) {
            g.fillRect(100, 100, 150, 100);
        } else if (shape.equals("oval")) {
            g.fillOval(100, 100, 150, 100);
        }
    }

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
    shape="oval";
    repaint();    // TODO add your handling code here:
    }                                        

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
    color= Color.RED;
    repaint();// TODO add your handling code here:
    }                                        

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
    shape= "rect";
    repaint();// TODO add your handling code here:
    }                                        

    private void jButton4ActionPerformed(java.awt.event.ActionEvent evt) {                                         
    color= Color.BLACK;
    repaint();// TODO add your handling code here:
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(JFrame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(JFrame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(JFrame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(JFrame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new JFrame1().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JButton jButton3;
    private javax.swing.JButton jButton4;
    // End of variables declaration                   
}
~~~

<img width="944" height="675" alt="image" src="https://github.com/user-attachments/assets/02c33472-0cec-4f20-8e56-cc7be540078b" />

## ASSIGNMENT-11
~~~
public class Frame2 extends javax.swing.JFrame {

    /**
     * Creates new form Frame2
     */
    public Frame2() {
        initComponents();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jButton1 = new javax.swing.JButton();
        jButton2 = new javax.swing.JButton();
        jButton3 = new javax.swing.JButton();
        jButton4 = new javax.swing.JButton();
        jTextField1 = new javax.swing.JTextField();
        jTextField2 = new javax.swing.JTextField();
        jTextField3 = new javax.swing.JTextField();
        jLabel1 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        jLabel3 = new javax.swing.JLabel();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jButton1.setText("ADD");
        jButton1.setToolTipText("");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        jButton2.setText("SUB");
        jButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton2ActionPerformed(evt);
            }
        });

        jButton3.setText("MUL");
        jButton3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton3ActionPerformed(evt);
            }
        });

        jButton4.setText("DIV");
        jButton4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton4ActionPerformed(evt);
            }
        });

        jTextField3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jTextField3ActionPerformed(evt);
            }
        });

        jLabel1.setText("Input1");

        jLabel2.setText("Input2");

        jLabel3.setText("Result");

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jButton4)
                    .addComponent(jButton3)
                    .addComponent(jButton2)
                    .addComponent(jButton1))
                .addGap(44, 44, 44))
            .addGroup(layout.createSequentialGroup()
                .addGap(34, 34, 34)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                    .addComponent(jLabel2, javax.swing.GroupLayout.PREFERRED_SIZE, 37, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel1, javax.swing.GroupLayout.PREFERRED_SIZE, 37, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel3, javax.swing.GroupLayout.PREFERRED_SIZE, 37, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(85, 85, 85)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                    .addComponent(jTextField1, javax.swing.GroupLayout.DEFAULT_SIZE, 95, Short.MAX_VALUE)
                    .addComponent(jTextField2)
                    .addComponent(jTextField3))
                .addContainerGap(149, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(31, 31, 31)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                    .addComponent(jLabel1)
                    .addComponent(jTextField1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(18, 18, 18)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jLabel2)
                    .addComponent(jTextField2, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(21, 21, 21)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jTextField3, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel3))
                .addGap(3, 3, 3)
                .addComponent(jButton1)
                .addGap(18, 18, 18)
                .addComponent(jButton2)
                .addGap(18, 18, 18)
                .addComponent(jButton3)
                .addGap(18, 18, 18)
                .addComponent(jButton4)
                .addContainerGap(15, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void jTextField3ActionPerformed(java.awt.event.ActionEvent evt) {                                            
        // TODO add your handling code here:
    }                                           

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
double a = Double.parseDouble(jTextField1.getText());
double b = Double.parseDouble(jTextField2.getText());

double result = a + b;
jTextField3.setText(String.valueOf(result));        // TODO add your handling code here:
    }                                        

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
double a = Double.parseDouble(jTextField1.getText());
double b = Double.parseDouble(jTextField2.getText());

double result = a - b;
jTextField3.setText(String.valueOf(result));        // TODO add your handling code here:
    }                                        

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
double a = Double.parseDouble(jTextField1.getText());
double b = Double.parseDouble(jTextField2.getText());

double result = a * b;
jTextField3.setText(String.valueOf(result));        // TODO add your handling code here:
    }                                        

    private void jButton4ActionPerformed(java.awt.event.ActionEvent evt) {                                         
double a = Double.parseDouble(jTextField1.getText());
double b = Double.parseDouble(jTextField2.getText());

if (b == 0) {
    jTextField3.setText("Cannot divide by 0");
} else {
    double result = a / b;
    jTextField3.setText(String.valueOf(result));
}        // TODO add your handling code here:
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(Frame2.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(Frame2.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(Frame2.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(Frame2.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new Frame2().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JButton jButton3;
    private javax.swing.JButton jButton4;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabel3;
    private javax.swing.JTextField jTextField1;
    private javax.swing.JTextField jTextField2;
    private javax.swing.JTextField jTextField3;
    // End of variables declaration                   
}
~~~

<img width="899" height="491" alt="image" src="https://github.com/user-attachments/assets/3ac17178-de17-41d7-94db-adb71ea13d4f" />

## ASSIGNMENT-12
~~~
import java.awt.Color;
import java.awt.Graphics;

public class world extends javax.swing.JFrame {

    Graphics g;

    private static final java.util.logging.Logger logger =
            java.util.logging.Logger.getLogger(world.class.getName());

    public world() {
        initComponents();
        g = this.getGraphics();
    }

    @SuppressWarnings("unchecked")
    private void initComponents() {

        jButton3 = new javax.swing.JButton();
        jSlider1 = new javax.swing.JSlider();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        addMouseMotionListener(new java.awt.event.MouseMotionAdapter() {
            public void mouseDragged(java.awt.event.MouseEvent evt) {
                formMouseDragged(evt);
            }
        });

        jButton3.setText("Color");
        jButton3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton3ActionPerformed(evt);
            }
        });

        jSlider1.addChangeListener(new javax.swing.event.ChangeListener() {
            public void stateChanged(javax.swing.event.ChangeEvent evt) {
                jSlider1StateChanged(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addComponent(jButton3)
            .addComponent(jSlider1)
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addComponent(jButton3)
            .addComponent(jSlider1)
        );

        pack();
    }

    private void formMouseDragged(java.awt.event.MouseEvent evt) {
        g.fillOval(evt.getX(), evt.getY(),
                jSlider1.getValue(), jSlider1.getValue());
    }

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {
        g.setColor(Color.RED);
    }

    private void jSlider1StateChanged(javax.swing.event.ChangeEvent evt) {
        System.out.println(jSlider1.getValue());
    }

    public static void main(String args[]) {
        java.awt.EventQueue.invokeLater(() -> {
            new world().setVisible(true);
        });
    }

    private javax.swing.JButton jButton3;
    private javax.swing.JSlider jSlider1;
}
~~~
<img width="724" height="955" alt="image" src="https://github.com/user-attachments/assets/6ebe5f41-b63a-4b6f-967d-30b98643bc4e" />

## ASSIGNMENT-13
~~~
class Division {
    int intDiv(int a, int b) {
        if (b == 0) throw new ArithmeticException("Divide by zero");
        return a / b;
    }

    double floatDiv(double a, double b) {
        if (b == 0) throw new ArithmeticException("Divide by zero");
        return a / b;
    }

    int remainder(int a, int b) {
        return a % b;
    }
}

public class Main1 {
    public static void main(String[] args) {
        Division d = new Division();

        try {
            System.out.println(d.intDiv(10, 2));
            System.out.println(d.floatDiv(5.5, 2));
            System.out.println(d.remainder(10, 3));
        } catch(Exception e) {
            System.out.println(e.getMessage());
        }
    }
}
~~~

<img width="794" height="356" alt="image" src="https://github.com/user-attachments/assets/fdbb47db-af85-4595-98cd-b0ce04b1dc4a" />

## ASSIGNMENT-14
~~~
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
public class studentform extends javax.swing.JFrame {

    /**
     * Creates new form studentform
     */
    public studentform() {
        initComponents();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jLabel1 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        jLabel3 = new javax.swing.JLabel();
        jLabel4 = new javax.swing.JLabel();
        txtId = new javax.swing.JTextField();
        txtName = new javax.swing.JTextField();
        txtCourse = new javax.swing.JTextField();
        txtMarks = new javax.swing.JTextField();
        jButton1 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jLabel1.setText("Student ID");

        jLabel2.setText("Name");

        jLabel3.setText("Course");

        jLabel4.setText("Marks");

        txtName.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                txtNameActionPerformed(evt);
            }
        });

        txtCourse.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                txtCourseActionPerformed(evt);
            }
        });

        txtMarks.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                txtMarksActionPerformed(evt);
            }
        });

        jButton1.setText("Register");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addGap(42, 42, 42)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                    .addComponent(jLabel4, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(jLabel1, javax.swing.GroupLayout.DEFAULT_SIZE, 68, Short.MAX_VALUE)
                    .addComponent(jLabel2, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(jLabel3, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addGap(117, 117, 117)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addComponent(txtCourse)
                            .addComponent(txtMarks)
                            .addGroup(layout.createSequentialGroup()
                                .addComponent(txtId, javax.swing.GroupLayout.PREFERRED_SIZE, 135, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addGap(0, 0, Short.MAX_VALUE))))
                    .addGroup(layout.createSequentialGroup()
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addComponent(txtName, javax.swing.GroupLayout.PREFERRED_SIZE, 135, javax.swing.GroupLayout.PREFERRED_SIZE)))
                .addGap(38, 38, 38))
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addComponent(jButton1)
                .addGap(74, 74, 74))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(50, 50, 50)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jLabel1)
                    .addComponent(txtId, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(31, 31, 31)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jLabel2)
                    .addComponent(txtName, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 31, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(txtCourse, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel3))
                .addGap(32, 32, 32)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(txtMarks, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel4))
                .addGap(18, 18, 18)
                .addComponent(jButton1)
                .addGap(27, 27, 27))
        );

        pack();
    }// </editor-fold>                        

    private void txtNameActionPerformed(java.awt.event.ActionEvent evt) {                                        
        // TODO add your handling code here:
    }                                       

    private void txtMarksActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
    }                                        

    private void txtCourseActionPerformed(java.awt.event.ActionEvent evt) {                                          
        // TODO add your handling code here:
    }                                         

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
try {
    Class.forName("com.mysql.cj.jdbc.Driver");
    Connection con = DriverManager.getConnection(
        "jdbc:mysql://localhost:3306/studentdb", "root", "root");

    String query = "INSERT INTO students VALUES (?, ?, ?, ?)";
    PreparedStatement pst = con.prepareStatement(query);

    pst.setInt(1, Integer.parseInt(txtId.getText()));
    pst.setString(2, txtName.getText());
    pst.setString(3, txtCourse.getText());
    pst.setInt(4, Integer.parseInt(txtMarks.getText()));

    pst.executeUpdate();

    javax.swing.JOptionPane.showMessageDialog(this, "Registered Successfully!");

    con.close();

} catch (Exception e) {
    javax.swing.JOptionPane.showMessageDialog(this, e);
}        // TODO add your handling code here:
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(studentform.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(studentform.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(studentform.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(studentform.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new studentform().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabel3;
    private javax.swing.JLabel jLabel4;
    private javax.swing.JTextField txtCourse;
    private javax.swing.JTextField txtId;
    private javax.swing.JTextField txtMarks;
    private javax.swing.JTextField txtName;
}
~~~

<img width="729" height="467" alt="image" src="https://github.com/user-attachments/assets/2882a4ab-ce63-4458-b30e-b88c9bed5fc4" />

## ASSIGNMENT-15
~~~
import java.awt.Graphics;
public class JFrame4 extends javax.swing.JFrame {

    /**
     * Creates new form JFrame4
     */
    public JFrame4() {
        initComponents();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jButton1 = new javax.swing.JButton();
        jButton2 = new javax.swing.JButton();
        jButton3 = new javax.swing.JButton();
        jButton4 = new javax.swing.JButton();
        jButton5 = new javax.swing.JButton();
        jButton6 = new javax.swing.JButton();
        jButton7 = new javax.swing.JButton();
        jButton8 = new javax.swing.JButton();
        jButton9 = new javax.swing.JButton();
        jButton10 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jButton1.setText("Rect");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        jButton2.setText("FillRect");
        jButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton2ActionPerformed(evt);
            }
        });

        jButton3.setText("Oval");
        jButton3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton3ActionPerformed(evt);
            }
        });

        jButton4.setText("FillOval");
        jButton4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton4ActionPerformed(evt);
            }
        });

        jButton5.setText("Line");
        jButton5.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton5ActionPerformed(evt);
            }
        });

        jButton6.setText("Text");
        jButton6.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton6ActionPerformed(evt);
            }
        });

        jButton7.setText("RoundRect");
        jButton7.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton7ActionPerformed(evt);
            }
        });

        jButton8.setText("FillRound");
        jButton8.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton8ActionPerformed(evt);
            }
        });

        jButton9.setText("Arc");
        jButton9.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton9ActionPerformed(evt);
            }
        });

        jButton10.setText("FillArc");
        jButton10.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton10ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addComponent(jButton5)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addComponent(jButton10))
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addComponent(jButton4)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addComponent(jButton9))
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addComponent(jButton3)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addComponent(jButton8))
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addComponent(jButton2)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 216, Short.MAX_VALUE)
                        .addComponent(jButton7))
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addComponent(jButton1)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addComponent(jButton6)))
                .addGap(18, 18, 18))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(23, 23, 23)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton1)
                    .addComponent(jButton6))
                .addGap(26, 26, 26)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton2)
                    .addComponent(jButton7))
                .addGap(27, 27, 27)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton3)
                    .addComponent(jButton8))
                .addGap(30, 30, 30)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton4)
                    .addComponent(jButton9))
                .addGap(29, 29, 29)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton5)
                    .addComponent(jButton10))
                .addContainerGap(50, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.drawRect(100, 250, 100, 80);        // TODO add your handling code here:
    }                                        

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.fillRect(100, 250, 100, 80);        // TODO add your handling code here:
    }                                        

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.drawOval(100, 250, 100, 80);        // TODO add your handling code here:
    }                                        

    private void jButton4ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.fillOval(100, 250, 100, 80);        // TODO add your handling code here:
    }                                        

    private void jButton5ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.drawLine(100, 250, 200, 350);        // TODO add your handling code here:
    }                                        

    private void jButton6ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.drawString("Hello", 150, 300);        // TODO add your handling code here:
    }                                        

    private void jButton7ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.drawRoundRect(100, 250, 120, 80, 20, 20);        // TODO add your handling code here:
    }                                        

    private void jButton8ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.fillRoundRect(100, 250, 120, 80, 20, 20);        // TODO add your handling code here:
    }                                        

    private void jButton9ActionPerformed(java.awt.event.ActionEvent evt) {                                         
Graphics g = getGraphics();
g.drawArc(100, 250, 100, 100, 0, 180);        // TODO add your handling code here:
    }                                        

    private void jButton10ActionPerformed(java.awt.event.ActionEvent evt) {                                          
Graphics g = getGraphics();
g.fillArc(100, 250, 100, 100, 0, 180);        // TODO add your handling code here:
    }                                         

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(JFrame4.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(JFrame4.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(JFrame4.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(JFrame4.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new JFrame4().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton10;
    private javax.swing.JButton jButton2;
    private javax.swing.JButton jButton3;
    private javax.swing.JButton jButton4;
    private javax.swing.JButton jButton5;
    private javax.swing.JButton jButton6;
    private javax.swing.JButton jButton7;
    private javax.swing.JButton jButton8;
    private javax.swing.JButton jButton9;
    // End of variables declaration                   
}
~~~

<img width="793" height="574" alt="image" src="https://github.com/user-attachments/assets/3e754171-f675-4319-9271-5aff6490c8bf" />

## ASSIGNMENT-16
~~~
class A {
    void show() {
        for (int i = 1; i <= 100; i++)
            System.out.println("A: " + i);
    }
}

class B {
    void show() {
        for (int i = 1; i <= 100; i++)
            System.out.println("B: " + i);
    }
}

class C {
    void show() {
        for (int i = 1; i <= 100; i++)
            System.out.println("C: " + i);
    }
}

public class Main11 {
    public static void main(String[] args) {
        new A().show();
        new B().show();
        new C().show();
    }
}
~~~

<img width="1224" height="419" alt="image" src="https://github.com/user-attachments/assets/fcba92f1-33b4-41ff-9719-cee4ac410c41" />

## ASSIGNMENT-17
~~~
public class Main12 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Test1 t1 = new Test1();
        Test2 t2 = new Test2();
        Test3 t3 = new Test3();

        t1.start();
        t2.start();
        t3.start();
    }
}

class Test1 extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("T1: " + i);
        }
    }
}

class Test2 extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("T2: " + i);
        }
    }
}

class Test3 extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("T3: " + i);
        }
    }
}
~~~

<img width="907" height="701" alt="image" src="https://github.com/user-attachments/assets/f150947a-177d-459b-a558-250c4c36a84f" />

## ASSIGNMENT-18
~~~
public class Main13 {
    public static void main(String[] args) {

        Testt1 t1 = new Testt1();
        Testt2 t2 = new Testt2();
        Testt3 t3 = new Testt3();

        Thread th1 = new Thread(t1);
        Thread th2 = new Thread(t2);
        Thread th3 = new Thread(t3);

        th1.start();
        th2.start();
        th3.start();
    }
}

class Testt1 implements Runnable {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("T1: " + i);
        }
    }
}

class Testt2 implements Runnable {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("T2: " + i);
        }
    }
}

class Testt3 implements Runnable {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("T3: " + i);
        }
    }
}
~~~
<img width="1280" height="688" alt="image" src="https://github.com/user-attachments/assets/89906644-4f22-475d-af32-4552c7f6c0d3" />

## ASSIGNMENT-19
~~~
BYTE-BY-BYTE
import java.io.*;

public class Main2 {
    public static void main(String[] args) {
        try {
            File input = new File("input.txt");

            if (!input.exists()) {
                System.out.println("Input file not found!");
                return;
            }

            FileInputStream fis = new FileInputStream(input);
            FileOutputStream fos = new FileOutputStream("output.txt");

            int i;
            while((i = fis.read()) != -1) {
                fos.write(i);
            }

            fis.close();
            fos.close();

            System.out.println("File copied successfully");
        } catch(Exception e) {
            System.out.println(e);
        }
    }
}

CHARACTER-BY-CHARACTER
import java.io.*;

public class Main3 {
    public static void main(String[] args) {
        try {
            FileReader fr = new FileReader("input.txt");
            FileWriter fw = new FileWriter("output.txt");

            int ch;

            while ((ch = fr.read()) != -1) {
                fw.write(ch);
            }

            fr.close();
            fw.close();

            System.out.println("File copied using character stream");
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
~~~

<img width="1118" height="361" alt="image" src="https://github.com/user-attachments/assets/e2ef12f9-a375-48af-bb61-1ba97a50c768" />

## ASSIGNMENT-20
~~~
import java.util.*;

public class Main4 {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();

        // Adding elements
        list.add("Apple");
        list.add("Banana");
        list.add("Mango");

        // Display
        System.out.println("List: " + list);

        // Remove element
        list.remove("Banana");

        // Search
        System.out.println("Contains Apple? " + list.contains("Apple"));

        // Update
        list.set(1, "Orange");

        // Iterate
        for(String item : list) {
            System.out.println(item);
        }
    }
}
~~~

<img width="912" height="351" alt="image" src="https://github.com/user-attachments/assets/22a2ce53-2025-4851-af64-ed3ccaef1d31" />

## ASSIGNMENT-21
~~~
import java.util.*;

public class Main5 {
    public static void main(String[] args) {
        LinkedList<Integer> list = new LinkedList<>();

        // Insert
        list.addFirst(10);
        list.addLast(30);
        list.add(1, 20); // middle

        // Display
        System.out.println("List: " + list);

        // Delete
        list.removeFirst();
        list.removeLast();

        // Search
        System.out.println("Contains 20? " + list.contains(20));

        // Display again
        for(int i : list) {
            System.out.println(i);
        }
    }
}
~~~

<img width="1305" height="403" alt="Screenshot 2026-04-27 213149" src="https://github.com/user-attachments/assets/abc6a190-5bf8-4940-b25c-69e1c2488bf8" />


## ASSIGNMENT-22
~~~
import java.util.*;

public class Main6 {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        // Push
        stack.push(10);
        stack.push(20);
        stack.push(30);

        // Peek
        System.out.println("Top: " + stack.peek());

        // Pop
        System.out.println("Popped: " + stack.pop());

        // Check empty
        System.out.println("Is empty? " + stack.isEmpty());

        System.out.println("Stack: " + stack);
    }
}
~~~

<img width="932" height="369" alt="image" src="https://github.com/user-attachments/assets/7f47882c-ae55-43cd-8f71-5b6f6695962b" />

## ASSIGNMENT-23
~~~
import java.util.*;

public class Main7 {
    public static void main(String[] args) {
        HashMap<Integer, String> map = new HashMap<>();

        // Insert
        map.put(1, "A");
        map.put(2, "B");
        map.put(3, "C");

        // Retrieve
        System.out.println("Key 2: " + map.get(2));

        // Remove
        map.remove(3);

        // Iterate
        for(Map.Entry<Integer, String> entry : map.entrySet()) {
            System.out.println(entry.getKey() + " -> " + entry.getValue());
        }
    }
}

~~~

<img width="801" height="351" alt="image" src="https://github.com/user-attachments/assets/94fdf003-efb7-4706-af9a-0b73190f9b3f" />

## ASSIGNMENT-24
~~~
import java.util.*;

public class Main8 {
    public static void main(String[] args) {
        TreeMap<Integer, String> map = new TreeMap<>();

        // Insert
        map.put(3, "C");
        map.put(1, "A");
        map.put(2, "B");

        // Sorted display
        System.out.println("Sorted Map: " + map);

        // Search
        System.out.println("Contains key 2? " + map.containsKey(2));

        // Remove
        map.remove(1);

        System.out.println("After removal: " + map);
    }
}
~~~

<img width="829" height="349" alt="image" src="https://github.com/user-attachments/assets/9b52fa87-16fc-4ece-a002-0e1359168200" />

## ASSIGNMENT-25
~~~
class StackArray {
    int top = -1;
    int max = 5;
    int[] stack = new int[max];

    void push(int x) {
        if (top == max - 1) {
            System.out.println("Stack Overflow");
        } else {
            stack[++top] = x;
        }
    }

    void pop() {
        if (top == -1) {
            System.out.println("Stack Underflow");
        } else {
            System.out.println("Popped: " + stack[top--]);
        }
    }

    void display() {
        for (int i = top; i >= 0; i--) {
            System.out.println(stack[i]);
        }
    }
}

public class Main9 {
    public static void main(String[] args) {
        StackArray s = new StackArray();

        s.push(10);
        s.push(20);
        s.push(30);

        s.display();

        s.pop();
        s.display();
    }
}
~~~

<img width="942" height="357" alt="image" src="https://github.com/user-attachments/assets/b938037d-5134-4de4-8bb5-b84fd3c54d21" />


