# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program using method overloading to print student details. Create a class Student with:

print(String name)

print(String name, int age)

print(String name, int age, String dept)

## AIM:
To create a Java program that demonstrates method overloading by printing student details using different versions of the same method

## ALGORITHM :
1.Start the program.

2.Create a class Student with three overloaded print() methods.

3.The first method prints only the name.

4.The second method prints name and age.

5.The third method prints name, age, and department.

6.In the main method, read the required inputs using Scanner.

7.Create a Student object and call the appropriate print() methods to display the details.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Raha Priya Dharshini M
RegisterNumber: 212224240124
import java.util.*;

class Student {

    void print(String name) {
        System.out.println("Name: " + name);
    }

    void print(String name, int age) {
        System.out.println("Name: " + name + ", Age: " + age);
    }

    void print(String name, int age, String dept) {
        System.out.println("Name: " + name + ", Age: " + age + ", Dept: " + dept);
    }
}

class prog {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();
        int age = sc.nextInt();
        sc.nextLine();
        String name3 = sc.nextLine();
        int age2 = sc.nextInt();
        sc.nextLine();
        String dept = sc.nextLine();

        Student s = new Student();

        s.print(name1);
        s.print(name2, age);
        s.print(name3, age2, dept);
    }
}

*/
```
## OUTPUT:



## RESULT:
The program successfully demonstrates method overloading by printing student details with different numbers of parameters.
