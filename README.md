import java.util.Scanner;

public class ManageEntity {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter action (create/update/delete): ");
        String action = scanner.nextLine();
        System.out.println("Enter entity name: ");
        String entityName = scanner.nextLine();
        if (action.equalsIgnoreCase("create")) {
            System.out.println("Creating entity: " + entityName);
        } else if (action.equalsIgnoreCase("update")) {
            System.out.println("Updating entity: " + entityName);
        } else if (action.equalsIgnoreCase("delete")) {
            System.out.println("Deleting entity: " + entityName);
        } else {
            System.out.println("Invalid action! Please try again.");
        }

        
        System.out.println("Do you want to perform another action? (yes/no): ");
        String confirm = scanner.nextLine();
        while (confirm.equalsIgnoreCase("yes")) {
            System.out.println("Enter action (create/update/delete): ");
            action = scanner.nextLine();
            System.out.println("Enter entity name: ");
            entityName = scanner.nextLine();

            if (action.equalsIgnoreCase("create")) {
                System.out.println("Creating entity: " + entityName);
            } else if (action.equalsIgnoreCase("update")) {
                System.out.println("Updating entity: " + entityName);
            } else if (action.equalsIgnoreCase("delete")) {
                System.out.println("Deleting entity: " + entityName);
            } else {
                System.out.println("Invalid action!");
            }

            System.out.println("Do you want to perform another action? (yes/no): ");
            confirm = scanner.nextLine();
        }

        System.out.println("Program terminated.");
    }
}
