# AIChatbot
Java Internship Project - AIChatbot
import java.util.HashMap;
import java.util.Scanner;

public class AIChatbot {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        HashMap<String, String> responses = new HashMap<>();

        responses.put("hello", "Hello! How can I help you?");
        responses.put("hi", "Hi! Nice to meet you.");
        responses.put("how are you", "I am fine. Thank you!");
        responses.put("java", "Java is an object-oriented programming language.");
        responses.put("internship", "Internships help students gain practical experience.");
        responses.put("project", "Projects improve coding skills.");
        responses.put("bye", "Goodbye! Have a great day.");

        System.out.println("================================");
        System.out.println("      AI CHATBOT STARTED");
        System.out.println("Type 'bye' to exit");
        System.out.println("================================");

        while (true) {

            System.out.print("\nYou: ");
            String input = sc.nextLine().toLowerCase();

            if (input.equals("bye")) {
                System.out.println("Bot: " + responses.get("bye"));
                break;
            }

            if (input.contains("hello")) {
                System.out.println("Bot: " + responses.get("hello"));
            }
            else if (input.equals("hi")) {
                System.out.println("Bot: " + responses.get("hi"));
            }
            else if (input.contains("how are you")) {
                System.out.println("Bot: " + responses.get("how are you"));
            }
            else if (input.contains("java")) {
                System.out.println("Bot: " + responses.get("java"));
            }
            else if (input.contains("internship")) {
                System.out.println("Bot: " + responses.get("internship"));
            }
            else if (input.contains("project")) {
                System.out.println("Bot: " + responses.get("project"));
            }
            else {
                System.out.println("Bot: Sorry, I don't understand. Please ask something else.");
            }
        }

        sc.close();
    }
}
