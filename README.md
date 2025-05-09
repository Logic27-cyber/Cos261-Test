#Cos261 Tests
Cos261 tests answers 

Basic & Syntax
1. Write a Java program to print "Hello, World".
   ANSWER
package cos261test;

public class Cos261Test {
    public static void main(String[] args) {
    //printing hello world
        System.out.println("Hello, World");
    }
}

run:
Hello, World
BUILD SUCCESSFUL (total time: 0 seconds)

![Screenshot (11)](https://github.com/user-attachments/assets/52c7426a-8dea-4a84-85e9-73ccc67dd274)

4. Write a Java program to add two numbers entered by the user.
   ANSWER
package cos261test;
import java.util.Scanner;

public class Cos261Test {
    public static void main(String[] args) {
    //initializing variables
        int number1, number2;
        int sum;
        //users input
        Scanner input = new Scanner(System.in);
        System.out.print("Enter first number : ");
        number1 = input.nextInt();
        System.out.print("Enter second number : ");
        number2 = input.nextInt();
        //addition of the numbers
        sum = number1 + number2;
        System.out.println("The sum of the two numbers are : " + sum);
    }
}

run:
Enter first number : 3
Enter second number : 4
The sum of the two numbers are : 7
BUILD SUCCESSFUL (total time: 3 seconds)

![Screenshot (12)](https://github.com/user-attachments/assets/2bb86b21-fd22-4767-baa0-16c0ebb7a2ff)

Control Structures
6. Write a program to check if a number is even or odd
   ANSWER
package cos261test;
import java.util.Scanner;

public class Cos261Test {
    public static void main(String[] args) {
    //initializing variable
        int number;
        //users input
        Scanner input = new Scanner(System.in);
        System.out.print("Enter number : ");
        number = input.nextInt();
        //if statement using modulo operator
        if (number % 2 == 0) {
        System.out.println("The number is even");
        }else{
        System.out.println("The number is odd");
        }
    }
}

run:
Enter number : 64
The number is even
BUILD SUCCESSFUL (total time: 4 seconds)

![Screenshot (13)](https://github.com/user-attachments/assets/f0f8583c-c962-4e07-bd3a-2a5e00161325)

7. Write a program to find the largest among three numbers.
   ANSWER
package cos261test;
import java.util.Scanner;

public class Cos261Test {
    public static void main(String[] args) {
    //initializing variables
      int number1,number2,number3; 
      //users input
      Scanner input = new Scanner (System.in);
      System.out.print("Enter first number : ");
      number1 = input.nextInt();
      System.out.print("Enter second number : ");
      number2 = input.nextInt();
      System.out.print("Enter third number : ");
      number3 = input.nextInt();
      //if eles statement comparing 3 numbers 
        if (number1 >= number2 && number1 >= number3) {
            System.out.print("number " + number1 + " is the largest number");
        }else if (number2 >= number1 && number2 >= number3) {
            System.out.print("number " + number2 + " is the largest number");
        }else {System.out.println("number " + number3 + " is the largest number");
        }
    }
}

run:
Enter first number : 1
Enter second number : 2
Enter third number : 3
number 3 is the largest number
BUILD SUCCESSFUL (total time: 5 seconds)

![image](https://github.com/user-attachments/assets/1d12e83d-974b-4551-a6d7-ac795fefa803)

9. Write a Java program to print the multiplication table of any number.
    ANSWER
package cos261test;
import java.util.Scanner;

public class Cos261Test {
    public static void main(String[] args) {
    //initializing variable
      int number1;  
      //users input
      Scanner input = new Scanner (System.in);
      System.out.print("Enter number : ");
      number1 = input.nextInt();
      System.out.print("Multiplication Table for " + number1 + " :");
      //for statement for multiplication
        for (int i = 0; i < 12; i++) {
            System.out.println(number1 + " x " + i + " = " + (number1 * i));
        }
    }
}

run:
Enter number : 5
Multiplication Table for 5 :5 x 0 = 0
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
5 x 11 = 55
BUILD SUCCESSFUL (total time: 2 seconds)

![Screenshot (16)](https://github.com/user-attachments/assets/de140ff4-fede-4c78-85cd-9e51a7d0d596)

OOP Concepts
11. Create a class student with properties name, matricNo, and score, and add method to display the student's info.
    ANSWER
package cos261test;

public class Cos261Test {
//properties of the student
    String name;
    String matricNo;
    double score;
    //constructor to intiliaze student
    public Cos261Test(String name, String matricNo, double score) {
    this.name = name;
    this.matricNo = matricNo;
    this.score = score;
    }
    //the method to diplay student info
    public void displayInfo(){
    System.out.print("Name :" + name);
    System.out.print("\nMatric Number :" + matricNo);
    System.out.print("\nScore : " + score);
    }
    //method of testing the class
    public static void main(String[] args) {
    //creating a student object with simple data
        Cos261Test stud = new Cos261Test(" Charles Kelvin", " 2022/241490", 90.5);
        //displaying the student's info
        stud.displayInfo();
        System.out.println();
    }
}

run:
Name :  Charles Kelvin
Matric Number :  2022/241490
Score : 90.5
BUILD SUCCESSFUL (total time: 0 seconds)

![Screenshot (17)](https://github.com/user-attachments/assets/2cd44536-46f6-4fee-b879-68025282c496)

12. What is method overloading? Give a code example
    ANSWER
package cos261test;

public class Cos261Test {
    // Method to add two integers
    public int add(int x, int y) {
        return x + y;
    }
    // Overloaded method to add three integers
    public int add(int x, int y, int z) {
        return x + y + z;
    }
    // Overloaded method to add two doubles
    public double add(double x, double y) {
        return x + y;
    }
    public static void main(String[] args) {
        Cos261Test calc = new Cos261Test();
        System.out.println(calc.add(2, 3));         // Outputs 5
        System.out.println(calc.add(1, 2, 3));      // Outputs 6
        System.out.println(calc.add(2.5, 3.5));     // Outputs 6.0
    }
}

run:
5
6
6.0
BUILD SUCCESSFUL (total time: 0 seconds)

![Screenshot (19)](https://github.com/user-attachments/assets/a9844e04-11c5-439a-bb91-cde78dcbc27c)


13. Create a base class Person and a subclass Teacher.
    ANSWER
package cos261test;

public class Cos261Test {
// here now u created the class Person like a blue print for creating a person 
public static class Person {
    String name;
    int age;
    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    // Method to display information
    public void displayInfo() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}   // this is the end of the person class

public static class Teacher extends Person {
    String department;
    String course;
    // Constructor for the teacher class
    public Teacher(String name, int age, String department, String course) {
        super(name,age);
    // super(age);
        this.department = department;
        this.course = course;
    }
    // you can add a method if u like 
}
    public static void main(String[] args) { 
    // TO SEE SMTH HAPPEN u can create a new instance of the class u just created
    Person person1 = new Person("Kelvin ", 24);
    System.out.println(person1.name + "Charles");
    person1.displayInfo();
    /* now u will see that we can create a new instance of a teacher class and
    it will inherit some attribute like name and age from person: if u check well u ll see that we didn't define name 
    and age for teacher but we fit call am or user am since its in Person that teacher inherited*/
    Teacher teacher1 = new Teacher("Aminat", 25, "Cos 261", "Computer Science");
    // now that we ve created it lets do smth with it
    System.out.println("Teacher " + teacher1.name + " Atanda" );
    teacher1.displayInfo();
    }
}
}

run:
Kelvin Charles
Name: Kelvin , Age: 24

Teacher Aminat Atanda
Name: Aminat, Age: 25
BUILD SUCCESSFUL (total time: 1 second)

![Screenshot (18)](https://github.com/user-attachments/assets/c8957f75-f104-4730-8bcc-38d309e36f13)

16. What naming conventions should be followed in Java for: Classes, Variables, Methods. Give examples with screenshot of code and output. 
    ANSWER
package cos261test;

public class Cos261Test {
    // Example 1
    String studentName = "Eze";
    int studentAge = 25;
    void displayInfo() {
        System.out.println("Student Name: " + studentName);
        System.out.println("Student Age: " + studentAge);
    }
    // Example 2
    String accountHolder = "Kelvin";
    double accountBalance = 400.95;
    void showBalance() {
        System.out.println("Account Holder: " + accountHolder);
        System.out.println("Balance: " + accountBalance);
    }
    // Example 3
    String carModel = "Ford";
    int carYear = 2023;
    void printDetails() {
        System.out.println("Car Model: " + carModel);
        System.out.println("Year: " + carYear);
    }
    public static void main(String[] args) {
        Cos261Test obj = new Cos261Test();
        obj.displayInfo();
        obj.showBalance();
        obj.printDetails();
    }
}

run:
Student Name: Eze
Student Age: 25
Account Holder: Kelvin
Balance: 400.95
Car Model: Ford
Year: 2023
BUILD SUCCESSFUL (total time: 1 second)

![Screenshot (20)](https://github.com/user-attachments/assets/b2279d06-f27e-49bb-bc03-e4e510cc364c)

18. Explain the concept of DRY (Don’t Repeat Yourself) with a Java code example
    ANSWER
package cos261test;

public class Cos261Test {
    // Reusable method
    static void greetUser(String name) {
        System.out.println("Welcome, " + name + "!");
    }
    public static void main(String[] args) {
        greetUser("Eze");
        greetUser("Kelvin");
        greetUser("Mary");
    }
}

run:
Welcome, Eze!
Welcome, Kelvin!
Welcome, Mary!
BUILD SUCCESSFUL (total time: 1 second)

![Screenshot (21)](https://github.com/user-attachments/assets/838c254b-4e63-48bd-9938-9173c3619070)

25. Write a sample Java method with JavaDoc comments. 
   ANSWER
package cos261test;

   /**
 * Utility class for number operations.
 */
public class Cos261Test {
    /**
     * Checks if a number is even.
     *
     * @param number the number to check
     * @return true if the number is even, false otherwise
     */
    public static boolean isEven(int number) {
        return numb % 2 == 0;
    }
    public static void main(String[] args) {
        System.out.println("Is 6 even? " + isEven(6));
        System.out.println("Is 3 even? " + isEven(3));
    }
}

run:
Is 6 even? true
Is 3 even? false
BUILD SUCCESSFUL (total time: 0 seconds)

![Screenshot (22)](https://github.com/user-attachments/assets/7194ede9-3ffb-4328-880e-510fef8f8045)

Mini Projects / Logic Building 

31. Build a command-line application that keeps track of student grades and allows adding, updating, and viewing records.
    ANSWER
package cos261test;
import java.util.HashMap;
import java.util.Scanner;

public class Cos261Test {
    public static void main(String[] args) {
        HashMap<String, String> records = new HashMap<>();
        Scanner input = new Scanner(System.in);
        System.out.println("Welcome to the Student Grade Tracker!");
        while (true) {
            System.out.println("\nWhat would you like to do?");
            System.out.println("1 - Add a student record");
            System.out.println("2 - Update a student's grade");
            System.out.println("3 - View all records");
            System.out.println("4 - Exit");
            System.out.print("Enter your choice (1-4): ");
            String choice = input.nextLine();
            if (choice.equals("1")) {
                System.out.print("Enter student name: ");
                String name = input.nextLine();
                if (records.containsKey(name)) {
                    System.out.println("This student already exists. Try updating instead.");
                } else {
                    System.out.print("Enter grade: ");
                    String grade = input.nextLine();
                    records.put(name, grade);
                    System.out.println("Student added successfully!");
                }
            } else if (choice.equals("2")) {
                System.out.print("Enter student name to update: ");
                String name = input.nextLine();
                if (records.containsKey(name)) {
                    System.out.print("Enter new grade: ");
                    String grade = input.nextLine();
                    records.put(name, grade);
                    System.out.println("Grade updated successfully!");
                } else {
                    System.out.println("Oops! That student doesn't exist.");
                }
            } else if (choice.equals("3")) {
                System.out.println("\n--- All Student Records ---");
                if (records.isEmpty()) {
                    System.out.println("No records yet. Try adding one!");
                } else {
                    for (String name : records.keySet()) {
                        System.out.println(name + " - " + records.get(name));
                    }
                }
            } else if (choice.equals("4")) {
                System.out.println("Thanks for using the tracker. Goodbye!");
                break;
            } else {
                System.out.println("Invalid option. Please pick 1, 2, 3, or 4.");
            }
        }
        input.close();
    }
}

run:
Welcome to the Student Grade Tracker!

What would you like to do?
1 - Add a student record
2 - Update a student's grade
3 - View all records
4 - Exit
Enter your choice (1-4): 1
Enter student name: Charles Kelvin
Enter grade: 89
Student added successfully!

What would you like to do?
1 - Add a student record
2 - Update a student's grade
3 - View all records
4 - Exit
Enter your choice (1-4): 3

--- All Student Records ---
Charles Kelvin - 89

What would you like to do?
1 - Add a student record
2 - Update a student's grade
3 - View all records
4 - Exit
Enter your choice (1-4): 4
Thanks for using the tracker. Goodbye!
BUILD SUCCESSFUL (total time: 2 minutes 18 seconds)

![Screenshot (26)](https://github.com/user-attachments/assets/bae62a60-6fca-4f74-a82e-cf650341706e)

32. Write a program that simulates a basic ATM system (check balance, deposit, withdraw). 
    ANSWER
package cos261test;
import java.util.Scanner;

public class Cos261Test {
    public static void main(String[] args) {
        double balance = 500.00;  // Starting balance
        Scanner input = new Scanner(System.in);
        System.out.println("Welcome to Kelvin-ATM!");
        while (true) {
            System.out.println("\n1. Check Balance");
            System.out.println("2. Deposit Money");
            System.out.println("3. Withdraw Money");
            System.out.println("4. Exit");
            System.out.print("Choose an option (1-4): ");
            String choice = input.nextLine();
            if (choice.equals("1")) {
                System.out.println("Your current balance is: $" + balance);
            } else if (choice.equals("2")) {
                System.out.print("Enter amount to deposit: $");
                double amount = input.nextDouble();
                input.nextLine(); // clear buffer
                if (amount > 0) {
                    balance += amount;
                    System.out.println("$" + amount + " deposited successfully.");
                } else {
                    System.out.println("Invalid deposit amount.");
                }
            } else if (choice.equals("3")) {
                System.out.print("Enter amount to withdraw: $");
                double amount = input.nextDouble();
                input.nextLine(); // clear buffer
                if (amount <= balance && amount > 0) {
                    balance -= amount;
                    System.out.println("$" + amount + " withdrawn successfully.");
                } else {
                    System.out.println("Insufficient funds or invalid amount.");
                }
            } else if (choice.equals("4")) {
                System.out.println("Thank you for banking with us. Goodbye!");
                break;
            } else {
                System.out.println("Invalid option. Please choose between 1–4.");
            }
        }
        input.close();
    }
}
    
run:
Welcome to Kelvin-ATM!

1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Choose an option (1-4): 1
Your current balance is: $500.0

1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Choose an option (1-4): 2
Enter amount to deposit: $5000000
$5000000.0 deposited successfully.

1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Choose an option (1-4): 3
Enter amount to withdraw: $1000000
$1000000.0 withdrawn successfully.

1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Choose an option (1-4): 1
Your current balance is: $4000500.0

1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Choose an option (1-4): 4
Thank you for banking with us. Goodbye!
BUILD SUCCESSFUL (total time: 36 seconds)

![Screenshot (27)](https://github.com/user-attachments/assets/d785be0f-5a63-4232-9e38-3f733fecde8c)



