Project Overview
The Virtual Classroom Manager is a command-line application designed to simulate basic classroom management activities, such as creating classrooms, adding students, scheduling assignments, and submitting assignments. It uses several software design patterns, including the Factory Pattern, Command Pattern, and Observer Pattern, to achieve modularity and extensibility.

Features
Classroom Management

Add new classrooms.
List all classrooms.
Student Enrollment

Add students to classrooms.
List students in a classroom.
Assignment Management

Schedule assignments for a classroom.
Submit assignments for students and notify observers (e.g., instructors) about the submission.
Notification System

Observers are notified whenever a student submits an assignment.
Design Patterns Used
Factory Pattern: Used to create instances of Classroom and Student via factories (ClassroomFactory and StudentFactory).
Command Pattern: Commands like adding classrooms, enrolling students, scheduling assignments, and submitting assignments are encapsulated in command objects.
Observer Pattern: The system notifies observers (e.g., AssignmentSubmissionNotifier) when an assignment is submitted.
Class Structure
Classroom: Represents a classroom with a list of students and assignments.
Student: Represents a student with a unique ID.
Assignment: Represents an assignment with details.
Factory Interface: Provides a generic method for creating objects.
Command Interface: Encapsulates an action or task to be executed.
AssignmentManager: Manages assignment submission and notifies observers.
AssignmentSubmissionNotifier: Concrete observer that responds to assignment submission events.
Commands: Various commands to manage classrooms, students, assignments, and notifications.
Getting Started
Prerequisites
Java Development Kit (JDK) 8 or above
An IDE or a command-line terminal with Java installed.
Running the Project
Clone or download the project files.
Open the project in your IDE or navigate to the project directory in your terminal.
Compile and run the VirtualClassroomManager.java file.
How to Use
Once the application is running, you can input commands in the following format:

Add Classroom:

php
Copy code
add_classroom <classroom_name>
Example:

Copy code
add_classroom Math101
Add Student:

php
Copy code
add_student <student_id> <classroom_name>
Example:

Copy code
add_student S001 Math101
Schedule Assignment:

php
Copy code
schedule_assignment <classroom_name> <assignment_details>
Example:

Copy code
schedule_assignment Math101 Chapter 1 Homework
Submit Assignment:

php
Copy code
submit_assignment <student_id> <classroom_name> <assignment_details>
Example:

Copy code
submit_assignment S001 Math101 Chapter 1 Homework
Command-Line Interaction
The application will continuously prompt for input, and you can issue commands.
Enter a command based on the operations described above.
You will get confirmation messages, or error messages if the command is invalid.
Example Commands
bash
Copy code
add_classroom Math101
add_student S001 Math101
schedule_assignment Math101 Chapter 1 Homework
submit_assignment S001 Math101 Chapter 1 Homework
Code Structure
Main Class: VirtualClassroomManager

This class contains the main method and handles user input.
Factories: ClassroomFactory, StudentFactory

Factories responsible for creating instances of Classroom and Student.
Commands: AddClassroomCommand, AddStudentCommand, ScheduleAssignmentCommand, SubmitAssignmentCommand

Encapsulate the operations that users can perform in the system.
Observer System: AssignmentManager, AssignmentSubmissionNotifier

Manages observers that get notified when an assignment is submitted.
