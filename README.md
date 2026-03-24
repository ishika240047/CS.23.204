# CS.23.204
[Program 7 : Abstract class](#xyz)
[Program 8 : final  ]
## xyz
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


