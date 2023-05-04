import java.util.Scanner;
public class JavaApplication70 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        boolean login = true;

        while (login) {
            System.out.println("LOG IN SYSTEM");
            System.out.print("Username: ");
            String uname = input.nextLine();
            System.out.print("Password: ");
            String pass = input.nextLine();

            String correctUname = "1";
            String correctPass = "2";

            if (uname.equals(correctUname) && pass.equals(correctPass)) {
                System.out.println("\nLOG IN SUCCESSFUL");
                login = false;
                break;
            } else {
                System.out.println("Invalid Username or Password");
            }

        }// while login

        boolean system = true;
        while (system) {


            System.out.println("\nMain Menu");
            System.out.println("[1] Check Attendance");
            System.out.println("[2] Logout");
            System.out.println("[3  Exit Program");
            System.out.print("\nEnter Option: ");
            String menu = input.nextLine();

            if (menu.equals("1")) {
                String[] studentNames = {"Abas", "Bacsarsa", "Cabol", "Dela Torre", "Gamon", "Jorigue", "Lusdoc", "Motizor", "Nerona", "Zaballero"};
                int[] absences = new int[10];
                int[] noShows = new int[10];
                int[] present = new int[10];

                for (int week = 1; week <= 7; week++) {
                    System.out.print("Do you want to take attendance for week " + week + "? (Y/N): ");
                    String proceed = input.nextLine();

                    while (!proceed.equalsIgnoreCase("y") && !proceed.equalsIgnoreCase("n")) {
                        System.out.print("Invalid input! Choose only Y or N: ");
                        proceed = input.next();
                    }

                    if (proceed.equalsIgnoreCase("n")) {
                        menu = "";
                        system = true;
                        break;

                    } else {
                        String date = "";
                        while (true) {
                            System.out.print("\nEnter Class Schedule Date (MM/DD/YYYY): ");
                            date = input.next();
                            if (date.matches("\\d{2}/\\d{2}/\\d{4}")) {
                                break;
                            } else {
                                System.out.println("Invalid date format. Please enter in MM/DD/YYYY format.");
                            }
                        }
                        int absentCount = 0;
                        int noShowCount = 0;
                        System.out.println("\n-*-Attendance Date: " + date);
                        System.out.println("\n[Type A for absent & P for Present]\n");
                        for (int i = 0; i < studentNames.length; i++) {
                            String studentName = studentNames[i];
                            System.out.print("Is " + studentName + " Present or Absent?: ");
                            String attendance = input.next().toUpperCase();
                            if (attendance.equals("P")) {
                                present[i]++;
                            } else if (attendance.equals("A")) {
                                absences[i]++;
                                absentCount++;
                                if (absences[i] >= 4) {
                                    noShows[i]++;
                                    noShowCount++;
                                }
                            } else {
                                System.out.println("Invalid input. Please enter P or A.");
                                i--;
                            }
                        }
                        System.out.println("Attendance Report for week " + week + ":");
                        System.out.println("+---------------+---------+--------+---------+");
                        System.out.println("|   Student     | Present | Absent | Status  |");
                        System.out.println("+---------------+---------+--------+---------+");
                        for (int i = 0; i < studentNames.length; i++) {
                            String studentName = studentNames[i];
                            int totalAbsences = absences[i];
                            int totalNoShows = noShows[i];
                            int totalPresent = present[i];
                            System.out.printf("| %-14s| %-8d| %-7d| %-8s|\n", studentName, totalPresent, totalAbsences, (totalNoShows >= 1 ? "NO SHOW" : " "));
                            System.out.println("+---------------+---------+--------+---------+");
                        }
                    }



                }// count sa students
            }// condition 1

            else if(menu.equals("2")){
                main(args);
                System.out.println("Logging out");
                system = false;
            } // condition 2
            else if(menu.equals("3")){
                System.exit(0);
            }// condition 3
           else{
                System.out.println("INVALID INPUT");
            }

        }// system while loop


    }
}
