import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        StudentDAO dao = new StudentDAO();
        Scanner sc = new Scanner(System.in);

        while (true) {
            System.out.println("\n--- Student Management System ---");
            System.out.println("1. Add Student");
            System.out.println("2. View All Students");
            System.out.println("3. Exit");
            System.out.print("Enter choice: ");
            int choice = sc.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter name: ");
                    String name = sc.next();
                    System.out.print("Enter age: ");
                    int age = sc.nextInt();
                    System.out.print("Enter course: ");
                    String course = sc.next();
                    dao.addStudent(name, age, course);
                    break;
                case 2:
                    dao.getAllStudents().forEach(s ->
                        System.out.println(s.getId() + " | " + s.getName() + " | " + s.getAge() + " | " + s.getCourse())
                    );
                    break;
                case 3:
                    System.out.println("Exiting...");
                    sc.close();
                    return;
                default:
                    System.out.println("Invalid choice!");
            }
        }
    }
}
