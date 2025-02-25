# getter-setter-methods-constructor-

Coding-

import java.io.*; 
class account { 
	private int balance = 50; 
             public int  account  (){
            return 0;


             }
		 
	 
	// accessor method (getter) 
	public int getBalance()  { 
		return balance; 
	} 
	// Mutator method (setter) 
	public void setBalance(int a) { 
	// return balance + a; 
		balance += a; 
	} 
} 
class balalceCalculate { 
    public static void main(String[] args) { 
	account obj = new account(); 
	obj.setBalance(50); 
	// calling the Mutator (accessor) 
System.out.println("Your Balance : "+ obj.getBalance()); 
   } 
}
 
//Constructor overloading
class Student5{  
    int id;
    String name;
    int age;  
    //creating two arg constructor  
    Student5(int i,String n){  
        id = i;
       name = n;  
    }  
    //creating three arg constructor  
    Student5(int i,String n,int a){  
    id = i;  
    name = n;  
    age=a;  
    }  
    void display(){
	System.out.println(id+" "+name+" "+age);
     }  
   
    public static void main(String args[]){  
       Student5 s1 = new Student5(111,"Abi");  
       Student5 s2 = new Student5(222,"Bhavana", 20);  
       s1.display();  
       s2.display();  
   }  
}
 class Employee {
    // Attributes
    private int employeeId;
    private String name;
    private double salary;

    // Constructor
    public Employee(int employeeId, String name, double salary) {
        this.employeeId = employeeId;
        this.name = name;
        this.salary = salary;
    }

    // Methods
    public int getEmployeeId() {
        return employeeId;
    }

    public String getName() {
        return name;
    }

    public double getSalary() {
        return salary;
    }

    public void increaseSalary(double percentage) {
        if (percentage > 0) {
            salary += salary * (percentage / 100);
            System.out.println("Salary increased by " + percentage + "%. New salary: $" + salary);
        } else {
            System.out.println("Invalid percentage. Salary remains unchanged.");
        }
    }
}

public class JavaApplication6 {
    public static void main(String[] args) {
        // Creating employees
Employee employee1 = new Employee(1, "Selvamathi", 50000.0);
        Employee employee2 = new Employee(2, " Gripsy", 60000.0);

        // Displaying employee information
        System.out.println("Employee 1: ID-" + employee1.getEmployeeId() + ", Name-" + employee1.getName() + ", Salary-$" + employee1.getSalary());
        System.out.println("Employee 2: ID-" + employee2.getEmployeeId() + ", Name-" + employee2.getName() + ", Salary-$" + employee2.getSalary());

        // Increasing salary for employee 1
        employee1.increaseSalary(10);

        // Increasing salary for employee 2 (invalid percentage)
        employee2.increaseSalary(-5);

        // Displaying updated employee information
        System.out.println("Updated Employee 1: Salary-$" + employee1.getSalary());
        System.out.println("Updated Employee 2: Salary-$" + employee2.getSalary());
    }
}


Output-

Employee 1: ID-1, Name-Selvamathi, Salary-$50000.0
Employee 2: ID-2, Name- Gripsy, Salary-$60000.0
Salary increased by 10.0%. New salary: $55000.0
Invalid percentage. Salary remains unchanged.
Updated Employee 1: Salary-$55000.0
Updated Employee 2: Salary-$60000.0
BUILD SUCCESSFUL (total time: 0 seconds)
