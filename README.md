# Student-record-using-array-
Practice program 
students = []
def insert_student():
    sid = raw_input("Enter Student ID: ")
    name = raw_input("Enter Student Name: ")
    marks = raw_input("Enter Marks: ") 
    students.append([sid, name, marks])
    print "Student record inserted"
def delete_student():
    sid = raw_input("Enter Student ID to delete: ")
       for s in students:
        if s[0] == sid:
            students.remove(s)
            print "Student record deleted"
            return
    print "Student not found"
def search_student():
    sid = raw_input("Enter Student ID to search: ")
    for s in students:
        if s[0] == sid:
            print "Student Found"
            print "ID:", s[0]
            print "Name:", s[1]
            print "Marks:", s[2]
            return
print "Student not found"
def display_students():
    if len(students) == 0:
        print "No records found"
    else:
        print "\nStudent Records"
        print "ID   Name   Marks"
        for s in students:
            print s[0], s[1], s[2]

while True:
    print "\n---- Student Record System ----"
    print "1. Insert Student"
    print "2. Delete Student"
    print "3. Search Student"
    print "4. Display Students"
    print "5. Exit"
    choice = int(raw_input("Enter your choice: "))
    if choice == 1:
        insert_student()
    elif choice == 2:
        delete_student()
    elif choice == 3:
        search_student()
    elif choice == 4:
        display_students()
    elif choice == 5:
        print "Program Ended"
break
    else:
        print "Invalid choice"
output:
1. Insert Student
2. Delete Student
3. Search Student
4. Display Students
5. Exit

Enter your choice: 1
Enter Student ID: 101
Enter Student Name: Ravi
Enter Marks: 85
Student record inserted
