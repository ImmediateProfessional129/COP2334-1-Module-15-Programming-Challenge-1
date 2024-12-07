# COP2334-1-Module-15-Programming-Challenge-1
This is a repository link of the COP2334-1 Module 15 Programming Challenge 1

// Shift supervisor Class

// This program is designed to print out the information of a new supervisor for a company. It will produce the name, salary, bonus, employee number, and the date they were hired.

#include <iostream> // Includes the iostream library
#include <string> // Includes the string library
using namespace std; // Assume the use of the standard (std) library

class Employee; // Declares the class Employee
class ShiftSupervisor; // Declares the class ShiftSupervisor

class Employee { // Declares the class Employee
private: // Private members of the class Employee
  string name; // Declares a string variable named name
  int number; // Declares an integer variable named number
  string employmentDate; // Declares a string variable named employmentDate
public: // Public members of the class Employee
  Employee(string n, int num, string date) { // Declares a constructor for the class Employee
    name = n; // Sets the value of name to n
    number = num; // Sets the value of number to num
    employmentDate = date; // Sets the value of employmentDate to date
  }
  string getName() { // Declares a function named getName that returns a string
    return name; // Returns the value of name
  }
  int getNumber() { // Declares a function named getNumber that returns an integer
    return number; // Returns the value of number
  }
  string getEmploymentDate() { // Declares a function named getEmploymentDate that returns a string
    return employmentDate; // Returns the value of employmentDate
  }
};

class ShiftSupervisor : public Employee { // Declares the class ShiftSupervisor that inherits from the class Employee
private: // Private members of the class ShiftSupervisor
  double salary; // Declares a double variable named salary
  double bonus; // Declares a double variable named bonus
public: // Public members of the class ShiftSupervisor
  ShiftSupervisor(string n, int num, string date, double s, double b) : Employee(n, num, date) { // Declares a constructor for the class ShiftSupervisor that inherits from the class Employee
    salary = s; // Sets the value of salary to s
    bonus = b; // Sets the value of bonus to b
  }
  double getSalary() { // Declares a function named getSalary that returns a double
    return salary; // Returns the value of salary
  }
  double getBonus() { // Declares a function named getBonus that returns a double
    return bonus; // Returns the value of bonus
  }
};

int main() { // The main function
  ShiftSupervisor supervisor("Jaylen Robinson", 3456, "5/17/1994", 50000, 10000); // Declares an object named supervisor of the class ShiftSupervisor
  cout << "Name: " << supervisor.getName() << endl; // Prints the name of the supervisor
  cout << "Employee Number: " << supervisor.getNumber() << endl; // Prints the employee number of the supervisor
  cout << "Hire Date: " << supervisor.getEmploymentDate() << endl; // Prints the hire date of the supervisor
  cout << "Salary: " << supervisor.getSalary() << endl; // Prints the salary of the supervisor
  cout << "Bonus: " << supervisor.getBonus() << endl; // Prints the bonus of the supervisor
  return 0; // Returns 0 to indicate successful program execution
}
