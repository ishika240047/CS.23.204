# CS.23.204
[ Program 1 : Write a program for addition ,subtractio, multiplication ,division using object and classes .](#program1)  

[ Program 2 : Write a class for addition of two distance where each distance is given in m,cm,mm.](#program2)  

[ Program 4 : Write a class for addition of two time given in hours, min and seconds.](#program4)  

[ Program 5 :  Write a program making a class for addition of two time given in hours and min Using Scanner class.](#program5)   

[ Program 7 : Write a class that is having four method for 1-dimensional array. (Input, output 1,ouput2, reverse).](#program7)  

## program1
```
class Calculator {
    int a, b;

    Calculator(int x, int y) {
        a = x;
        b = y;
    }

    void add() {
        System.out.println("Addition = " + (a + b));
    }

    void sub() {
        System.out.println("Subtraction = " + (a - b));
    }

    void mul() {
        System.out.println("Multiplication = " + (a * b));
    }

    void div() {
        if (b != 0)
            System.out.println("Division = " + (a / b));
        else
            System.out.println("Cannot divide by zero");
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator obj = new Calculator(10, 5);
        obj.add();
        obj.sub();
        obj.mul();
        obj.div();
    }
}
```
<img width="165" height="119" alt="Screenshot 2026-04-22 114826" src="https://github.com/user-attachments/assets/aa0cbc0b-c181-41f5-8b34-e3ee03c332fa" />  

## program2
```
class Distance {
    int m, cm, mm;

    Distance(int m, int cm, int mm) {
        this.m = m;
        this.cm = cm;
        this.mm = mm;
    }

    void add(Distance d2) {
        int total_mm = this.mm + d2.mm;
        int total_cm = this.cm + d2.cm + total_mm / 10;
        total_mm %= 10;

        int total_m = this.m + d2.m + total_cm / 100;
        total_cm %= 100;

        System.out.println("Result = " + total_m + "m " + total_cm + "cm " + total_mm + "mm");
    }
}

public class Distance1 {
    public static void main(String[] args) {
        Distance d1 = new Distance(2, 50, 5);
        Distance d2 = new Distance(3, 70, 8);

        d1.add(d2);
    }
}


```
## Output :

<img width="1454" height="42" alt="Screenshot 2026-04-22 141000" src="https://github.com/user-attachments/assets/1e27f6ae-682a-4875-b884-581160a51925" />


---

## program4 
### Write a class for addition of two time given in hours, min and seconds
```
class Time1 {
    int h, m, s;

    Time1(int h, int m, int s) {
        this.h = h;
        this.m = m;
        this.s = s;
    }

    void add(Time1 t2) {
        int sec = this.s + t2.s;
        int min = this.m + t2.m + sec / 60;
        sec = sec % 60;

        int hr = this.h + t2.h + min / 60;
        min = min % 60;

        System.out.println("Result Time = " + hr + " hr " + min + " min " + sec + " sec");
    }
}

public class Time {
    public static void main(String[] args) {

        Time1 t1 = new Time1(2, 45, 50);
        Time1 t2 = new Time1(3, 20, 30);

        t1.add(t2);
    }
}
```
## Output 
<img width="1345" height="41" alt="Screenshot 2026-04-22 142231" src="https://github.com/user-attachments/assets/b4d93149-0958-4d72-af10-ddc131cdf8f8" />
---  

## program5  

### Write a program making a class for addition of two time given in hours, min using Scanner class.  

```
import java.util.*;
class TimeHM {
    int h1, m1,h2,m2;

   
    void input(){
    Scanner sc  = new Scanner(System.in);
    System.out.println("enter the time in hour");
     h1 = sc.nextInt();
    System.out.println("enter the time in minutes");
    m1 = sc.nextInt();  
    System.out.println("enter the time in hour");
     h2 = sc.nextInt();
    System.out.println("enter the time in minutes");
    m2 = sc.nextInt(); 
         }

    
    void add() {

       
        int totalMin = m1 + m2;

        
        int extraHour = totalMin / 60;

        
        int finalMin = totalMin % 60;

        
        int finalHour = h1 + h2 + extraHour;

        
        System.out.println("Final Time = " + finalHour + " hours " + finalMin + " minutes");
    }
}


public class TimeH {
    public static void main(String[] args) {

 
        TimeHM t1 = new TimeHM();
        

        t1.input();
        t1.add();
    }
}
```
## Output

<img width="1407" height="226" alt="Screenshot 2026-04-23 155906" src="https://github.com/user-attachments/assets/6cbc1550-e848-4dc7-a750-471e358f5b6a" />

---  

## program7

## Program 7  : Write a class that is having four method for 1-dimensional array. (Input, output 1,output 2, reverse  .

```
import java.util.Scanner;

class ArrayOps {
    int arr[] = new int[5];   

   
    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter 5 elements:");

        for(int i = 0; i < arr.length; i++) {
            arr[i] = sc.nextInt();
        }
    }

    
    void output1() {
        System.out.println("Output using for loop:");

        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    // Method 3: Output using for-each loop
    void output2() {
        System.out.println("Output using for-each loop:");

        for(int x : arr) {
            System.out.print(x + " ");
        }
        System.out.println();
    }

    
    void reverse() {
        System.out.println("Array in reverse:");

        for(int i = arr.length - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}


public class Arr {
    public static void main(String[] args) {

        ArrayOps obj = new ArrayOps();

        obj.input();
        obj.output1();
        obj.output2();
        obj.reverse();
    }
}
```

## Output : 
<img width="1722" height="530" alt="Screenshot 2026-04-24 134634" src="https://github.com/user-attachments/assets/daa8113f-aecc-47db-9955-8a38b6e5e169" />


---  

## Program 9 : Write a program using three classes to print 1-100,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface.
### Without Thread
```
class Cls1{
void run(){
    for(int i = 0;i<100;i++){
    System.out.println(i+" from class1");}
}
}
class Cls2{
void run(){
     for(int i = 0;i<100;i++){
    System.out.println(i+" from class2 ");}
}
}
class Cls3{
void run(){
     for(int i = 0;i<100;i++){
    System.out.println(i+" from class3 ");}
}
}

public class IshiTred {
    public static void main (String[] args){
       Cls1 obj1 = new Cls1();
       Cls2 obj2 = new Cls2();
       Cls3 obj3 = new Cls3();

       obj1.run();
       obj2.run();
       obj3.run();
    }
}

```
## OUTPUT 
0 from class1<br>
1 from class1<br>
2 from class1<br>
3 from class1<br>
..........................<br>
..........................<br>
99 from class1<br>
1 from class2<br>
.............................<br>
.............................<br>

### Using Thread
```
class Cls1 extends Thread{
public void run(){
    for(int i = 0;i<100;i++){
    System.out.println(i+" from class1");}
}
}
class Cls2 extends Thread{
public void run(){
     for(int i = 0;i<100;i++){
    System.out.println(i+" from class2 ");}
}
}
class Cls3 extends Thread{
public void run(){
     for(int i = 0;i<100;i++){
    System.out.println(i+" from class3 ");}
}
}
public class IshiTred2 {
    public static void main(String[] args){
        Cls1 obj1 = new Cls1();
       Cls2 obj2 = new Cls2();
       Cls3 obj3 = new Cls3();

       obj1.start();
       obj2.start();
       obj3.start();
    }
}
```
## OUTPUT 
0 from class1 <br>
0 from class3 <br>
0 from class2 <br>
1 from class1<br>
1 from class3 <br>
2 from class3 <br>
3 from class3 <br>
1 from class2 <br>
2 from class1 <br>
.......................<br>
........................<br>

### Using Runnable interface
```
class Cls1 implements Runnable {
public void run(){
    for(int i = 0;i<100;i++){
    System.out.println(i+" from class1");}
}
}
class Cls2 implements Runnable{
public void run(){
     for(int i = 0;i<100;i++){
    System.out.println(i+" from class2 ");}
}
}
class Cls3 implements Runnable{
public void run(){
     for(int i = 0;i<100;i++){
    System.out.println(i+" from class3 ");}
}
}
public class IshiTred3 {

    public static void main(String[] args) {
        
    
     Cls1 obj1 = new Cls1();
       Cls2 obj2 = new Cls2();
       Cls3 obj3 = new Cls3();

       Thread t1 = new Thread(obj1);
        Thread t2 = new Thread(obj2);
        Thread t3 = new Thread(obj3);

        t1.start();
        t2.start();
        t3.start();
}
}
```
## OUTPUT 
0 from class1<br>
0 from class3 <br>
0 from class2 <br>
1 from class1<br>
1 from class3 <br>
2 from class3 <br>
3 from class3 <br>
1 from class2 <br>
2 from class1 <br>
.........................<br>
...........................<br>
[Program 7 : Abstract class]
[Program 8 : final  ](#mno)

```abstract class Salary //abstract class
	    {
		int perMonth=500000;
		int perHour=2000,amount;
		abstract void calculate(); //abstract method
	    }
class Monthly extends Salary
	   {
		int noOfMonths;
		Monthly(int nom)
		      {
			noOfMonths=nom;
		      }
		void calculate() //method overriding 
		      {
			int amount = noOfMonths*perMonth;
		        System.out.println("No. Of Months:"+ noOfMonths);
			System.out.println("Total Amount:" +amount);
		      }
	   }
class Hourly extends Salary
            {
		int noOfHours;
		Hourly(int h)
		    {
			noOfHours=h;
		    }	
void calculate() //method overriding
		{
			int amount=noOfHours*perHour;
			System.out.println("No. Of Hours: "+noOfHours);
			System.out.println("Total Amount:" +amount);
		}
      }
public class AbDemo 
     {
	public static void main(String[] args) 
	   {
		Hourly h=new Hourly(1000);
		h.calculate();
		Salary m=new Monthly(6);
		m.calculate();
	   }
    }```
Output
<img width="204" height="88" alt="image" src="https://github.com/user-attachments/assets/bc7ad64c-05a6-4afc-a4d8-edd03ae00dfa" />

## mno
class Superclass {
    //final variable 
    final int i = 10 ;
    //final method 
    final void display(){
        System.out.println("Super class method ");
        System.out.println("final variable " + i);
    }
}


public class Final extends Superclass {
    void display(int i ){
        System.out.println("you are in the method of the child class");
    }
public static void main(String[] args) {
    Final obj = new Final();
    obj.display(10);
}
}


