import java.util.ArrayList;
import java.util.Scanner;
// Class to store alumni details
class Alumni {
 private String name;
 private String yearOfGraduation;
 private String course;
 private String email;
 // Constructor
 public Alumni(String name, String yearOfGraduation, String course, String email) 
{
 this.name = name;
 this.yearOfGraduation = yearOfGraduation;
 this.course = course;
 this.email = email;
 }
 // Getter methods
 public String getName() {
 return name;
 }
 public String getYearOfGraduation() {
 return yearOfGraduation;
 }
 public String getCourse() {
 return course;
 }
// Method to display all alumni details
 public void displayAlumni() {
 if (alumniList.isEmpty()) {
 
 System.out.println("No alumni data available.\n");
 return;
 }
 System.out.println("Alumni List:");
 for (Alumni alumni : alumniList) {
 alumni.displayDetails();
 }
 }
 // Method to search alumni by name
 public void searchAlumniByName(String name) {
 boolean found = false;
 for (Alumni alumni : alumniList) {
 if (alumni.getName().equalsIgnoreCase(name)) {
 alumni.displayDetails();
 found = true;
 }
 }
 if (!found) {
 System.out.println("Alumni not found with name: " + name + "\n");
 }
 }
 // Main method
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
// Method to display all alumni details
 public void displayAlumni() {
 if (alumniList.isEmpty()) {
 
 System.out.println("No alumni data available.\n");
 return;
 }
 System.out.println("Alumni List:");
 for (Alumni alumni : alumniList) {
 alumni.displayDetails();
 }
 }
 // Method to search alumni by name
 public void searchAlumniByName(String name) {
 boolean found = false;
 for (Alumni alumni : alumniList) {
 if (alumni.getName().equalsIgnoreCase(name)) {
 alumni.displayDetails();
 found = true;
 }
 }
 if (!found) {
 System.out.println("Alumni not found with name: " + name + "\n");
 }
 }
 // Main method
 public static void main(String[] args) {
 Scanner scanner = new Scanner(System.in);
AlumniManagementSystem system = new AlumniManagementSystem();
 while (true) {
 System.out.println("Alumni Management System");
 System.out.println("1. Add Alumni");
 System.out.println("2. Display Alumni");
 System.out.println("3. Search Alumni by Name");
 
 System.out.println("4. Exit"); 
 System.out.print("Choose an option: ");
 int option = scanner.nextInt();
 scanner.nextLine(); // Consume newline
 switch (option) {
 case 1:
 System.out.print("Enter Alumni Name: ");
 String name = scanner.nextLine();
 System.out.print("Enter Year of Graduation: ");
 String year = scanner.nextLine();
 System.out.print("Enter Course: ");
 String course = scanner.nextLine();
 System.out.print("Enter Email: ");
 String email = scanner.nextLine();
 system.addAlumni(name, year, course, email);
 break;
 case 2:
 system.displayAlumni();
 break;
case 3:
 System.out.print("Enter Alumni Name to Search: ");
 String searchName = scanner.nextLine();
 system.searchAlumniByName(searchName);
 break;
 case 4:
 System.out.println("Exiting...");
 scanner.close();
 return;
 default:
 System.out.println("Invalid option! Please choose again.\n");
 }
 }
 }
}
