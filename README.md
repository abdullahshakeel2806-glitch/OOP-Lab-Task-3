# OOP-Lab-Task-3

class Employee {

    String name;
    double salary;

    // Parameterized constructor
    Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }

    void displayDetails() {
        System.out.println("Employee Name: " + name);
        System.out.println("Salary: " + salary);
    }
}

class Manager extends Employee {

    String department;

    // Constructor using super
    Manager(String name, double salary, String department) {
        super(name, salary);
        this.department = department;
    }

    // Method overriding
    @Override
    void displayDetails() {
        System.out.println("Manager Name: " + name);
        System.out.println("Salary: " + salary);
        System.out.println("Department: " + department);
    }
}

public class Main {
    public static void main(String[] args) {

        Manager m = new Manager(
            "Abdullah", 80000, "IT"
        );

        m.displayDetails();
    }
}
