Download Link: https://assignmentchef.com/product/solved-cse240-homework10-c-inheritance-and-polymorphism
<br>
Introduction

The aim of this assignment is to make sure that you understand and are familiar with the concepts covered in the lectures, including C++ inheritance, polymorphism, virtual function, containment, file operations, and exception handling. By the end of the assignment, you should have understood

<ul>

 <li>Class, data members, function members, virtual function, constructor, and destructor</li>

 <li>Accessing privileges among the classes</li>

 <li>Memory management and deletion of linked list</li>

 <li>Scope Resolution Operators</li>

 <li>Inheritance and containment</li>

 <li>Dynamic binding and polymorphism</li>

 <li>File operations</li>

 <li>Exception handling</li>

</ul>




<strong>Reading</strong>:​ Textbook Chapter 3, Sections 3.2 through 3.5. Read Section 3.2.1 on friend access. Read the program example in Section 3.4.2.

<strong>Preparation</strong>:​ Complete the multiple choice questions in the textbook exercise section. The answer keys can be found in the course Web site. These exercises can help you prepare for your weekly quiz and the exam. You are encouraged to read the other exercise questions and make sure that you understand these questions in the textbook exercise section, which can help you better understand what materials are expected to understand after the lectures and homework on each chapter.

You are expected to do the majority of the assignment outside the class meetings. Should you need assistance, or have questions about the assignment, please contact the instructor or the TA during their office hours.

You are encouraged to ask and answer questions on the course discussion board. However, <strong>do</strong>​<strong> not share your answers and code</strong> in the course discussion board.​

Programming Exercise

You are given a partially completed project containing:

<ul>

 <li><u>header files:</u> h student.h undergrad.h</li>

</ul>

grad.h

<ul>

 <li><u>C++ files:</u></li>

</ul>

Container.cpp student.cpp grad.cpp undergrad.cpp

hw10.cpp

The diagram shows the inheritance and relationships between the classes and the linked list formed.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/05/228.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/05/228.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>




Your job is to follow the instructions given in comments in these files to complete the missing parts of the project so that the program executes properly. Tasks are included below.

Q1: Create Undergrad and Grad subclasses of Student class (Inheritance) (10 points)

<u>In undergrad.h:</u>

// Q1a: Create Undergrad class (5 points)

// Part 1: Create a child class of the Student class named ‘Undergrad’

// Part2: Declare constructor which accepts the same 3 parameters as the parent class Student’s constructor.  Pass the 3 parameters to the super constructor of the Student class. // Part 3: Re-declare the method displayInfo (virtual method found inside of parent class Student)

<u>In grad.h:</u>

// Q1b: Create Grad class (5 points)

// Part 1: Create a child class of the Student class named ‘Grad’

// Part2: Declare constructor which accepts the same 3 parameters as the parent class Student’s constructor. Pass the 3 parameters to the super constructor of the Student class. // Part 3: Re-declare the method displayInfo (virtual method found inside of parent class Student)

Q2: Define displayInfo() for child classes (Polymorphism) (10 points)

<u>In undergrad.cpp</u>

// Q2a: Define displayInfo() for Undergrad class (5 points)

// Define the function displayInfo() that you declared within the Undergrad class in the header file. See expected output in question file

<u>In grad.cpp</u>

// Q2b: Define displayInfo() for Grad class (5 points)

// Define the function displayInfo() that you declared within the Grad class in the header file // See expected output in question file.

Q3: Add Friend function changeRollNo() (5 points)

<u>In student.h:</u>

// Q3a: Declare Friend Function changeRollNo()  (1 point)

// Declare a friend function named changeRollNo() which has 2 parameters and no return value.

// The first parameter is a pointer to Student class, and the second is an integer which is the new roll number.

// You need to define this function in hw10.cpp and call this function in case ‘c’ of executeAction() in hw10.cpp file

<u>In hw10.cpp:</u>

// Q3b: Define Friend Function changeRollNo()  (3 points)

// Define the function changeRollNo()that is declared in student.h file.

// This function sets the new roll number of the student. The student and new roll number is to be passed as function arguments.

// Use ‘d’ display option after using ‘c’ option to verify whether the new roll number is set.




A “friend function” allows you to access the private variables of a class (ex: student-&gt;rollNo) <strong>Q4 – Q7</strong> are used to implement a menu-driven program. Its implementation is in hw10.cpp.​            The menu gives the following options to user:

<ol>

 <li>Add a new student to the list. You need not check if the student exists in the list because that is already implemented in executeAction(). You may add the new student to head or tail of the list. (sample solution adds it to the tail)</li>

 <li>Display the list of students along with their details (roll number, type (grad/undergrad)).</li>

 <li>Change the roll number of a student. This options uses the friend function changeRollNo() to access private data member ‘rollNo’ of the student and change it to the one entered by the user.</li>

</ol>




You need to implement save() that writes the list of students to a file ‘list.txt’ while exiting the program and load() that reads the file to form the list at the beginning of the program. During first execution of the program, there will be no ‘list.txt’, so load() would not form a list. Once list.txt is saved, load() can read it. You may remove the list.txt from your project directory if you do not want to load that list (maybe while testing your code).

The following is one way to store the list in list.txt file. The format here is:

student name student roll number

student type (0 for undergrad, 1 for grad)

You may store it in another format if you wish. Notice that the ‘3’ at the beginning is the number of students stored in the file.


