[Program-1 WAP to add three distances](#ass-01)

[Program-2 WAP Hierchialclass](#ass-02)

[Program-3 WAP inheritclass ](#ass-03)


## ass-01
```
import java.util.Scanner;

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */

/**
 *
 * @author IBM31
 */
public class twoDARRAY {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        two A = new two();
        A.input();
        A.output();
    }
    
}
class two{
    int x[][];
    Scanner sc = new Scanner(System.in);
    
    two(){
        x = new int[2][2];
    }
    void input(){
        for( int i=0;i<2;i++)
            for(int j =0;j<2;j++)
                x[i][j] = sc.nextInt();
    }
    void output(){
        for( int i=0;i<2;i++){
            for(int j =0;j<2;j++){
                System.out.print(x[i][j] +" ");
            }
            System.out.println(" ");
        }
    }
}
```
<img width="1280" height="1024" alt="image" src="https://github.com/user-attachments/assets/316a1cd0-cbfa-44c9-bb85-bc0a91dec75b" />


## ass-02
```
public class Hierchialclass {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        A O1 = new A();
        B O2 = new B();
        C O3 = new C();
        O1.fun1();
        O2.fun2();
        O3.fun3();
    }
    
}

class A{
    void fun1(){
        System.out.println("We are in A");
    }
}

class B extends A{
    void fun2(){
        System.out.println("We are in class B");
    }
}
class C extends A{
    void fun3(){
        System.out.println("We are in class C");
    }
}
```
<img width="1280" height="1024" alt="image" src="https://github.com/user-attachments/assets/a0ed4b2e-00ef-4323-8ee9-37f0beac5191" />

## ass-03
```
public class inheritclass {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        testA A = new testA();
        testB B = new testB();
        testC C = new testC();
        
        A.fun1();
        C.fun3();
        B.fun2();
    }
    
}
class testA{
    void fun1(){
        System.out.println("You are in class A");
    }
    
}
class testB extends testA{
    void fun2(){
        System.out.println("You are in class B");
    }
} 

class testC extends testB{
    void fun3(){
        System.out.println("You are in class C");
    }
    
}
```
<img width="1280" height="1024" alt="image" src="https://github.com/user-attachments/assets/1912906f-1957-48b2-812a-56942c6a6287" />


