
import java.util.Scanner;

class Student {
    String name;
    int rollNo;
    String course;
    double fee;

    Student(String name, int rollNo, String course, double fee) {
        this.name = name;
        this.rollNo = rollNo;
        this.course = course;
        this.fee = fee;
    }

    void displayDetails() {
        System.out.println("Name: " + name);
        System.out.println("Roll No: " + rollNo);
        System.out.println("Course: " + course);
        System.out.println("Fee: " + fee);
    }
}

public class StudentDetails {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter number of students: ");
        int n = scanner.nextInt();

        Student[] students = new Student[n];

        for (int i = 0; i < n; i++) {
            System.out.print("Enter name of student " + (i + 1) + ": ");
            String name = scanner.next();

            System.out.print("Enter roll no of student " + (i + 1) + ": ");
            int rollNo = scanner.nextInt();

            System.out.print("Enter course of student " + (i + 1) + ": ");
            String course = scanner.next();

            System.out.print("Enter fee of student " + (i + 1) + ": ");
            double fee = scanner.nextDouble();

            students[i] = new Student(name, rollNo, course, fee);
        }

        scanner.close();

        for (int i = 0; i < n; i++) {
            System.out.println("\nDetails of Student " + (i + 1));
            students[i].displayDetails();
        }
    }
}


Output:


Enter number of students: 2
Enter name of student 1: John
Enter roll no of student 1: 101
Enter course of student 1: Java
Enter fee of student 1: 5000
Enter name of student 2: Alice
Enter roll no of student 2: 102
Enter course of student 2: Python
Enter fee of student 2: 6000

Details of Student 1
Name: John
Roll No: 101
Course: Java
Fee: 5000.0

Details of Student 2
Name: Alice
Roll No: 102
Course: Python
Fee: 6000.0
# Student-details-
