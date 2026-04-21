# CS.23.204
[Program 9 : Write a program using three classes to print 1-100,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface.]
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
0 from class1
1 from class1
2 from class1
3 from class1
.............
.............
99 from class1
1 from class2
.............
.............

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
0 from class1
0 from class3 
0 from class2 
1 from class1
1 from class3 
2 from class3 
3 from class3 
1 from class2 
2 from class1 
.............
.............

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
0 from class1
0 from class3 
0 from class2 
1 from class1
1 from class3 
2 from class3 
3 from class3 
1 from class2 
2 from class1 
.............
.............
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


