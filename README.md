# Email-Slicer-and-Username-Suggester-
    import java.util.Scanner;
    import java.util.Random;

    public class Main {
     public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        System.out.print("Please Enter Your Email: ");
        String email = scanner.nextLine();

        if (email.contains("@") && email.indexOf("@") > 0) {
            int atIndex = email.indexOf("@");
            String username = email.substring(0, atIndex);
            String domain = email.substring(atIndex + 1);

            int randomNum = random.nextInt(10, 99); 
            String suggestion = username + randomNum;

            System.out.println("Suggested Username: " + suggestion);
            System.out.print("Enter Desired Username: ");
            String usernameFr = scanner.nextLine();

            System.out.println("-----------------------------------------");
            System.out.println("Email:    " + email);
            System.out.println("Username: " + usernameFr);
            System.out.println("Domain:   " + domain);
            System.out.println("-----------------------------------------");
        } else {
            System.out.println(">> Error: A valid email must contain '@' after the username.");
        }

        scanner.close();
    }
}
