# Candy Machine
    import java.util.Scanner;

    public class CandyMachine {
    
    public static Scanner input = new Scanner(System.in);
    public static String again;
    public static int choose,quantity=1;
    public static double total=0,pay;
    public static void menu(){
    System.out.println("\t\t\t\t+===================================+");
    System.out.println("\t\t\t\t           CANDY MACHINE             ");
    System.out.println("\t\t\t\t   1. Candies              Php. 15.00");
    System.out.println("\t\t\t\t   2. Chips                Php. 10.00");
    System.out.println("\t\t\t\t   3. Gum                  Php. 5.00");
    System.out.println("\t\t\t\t   4. Cookies              Php. 15.00");
    System.out.println("\t\t\t\t   5. CANCEL                         ");
    System.out.println("\t\t\t\t+====================================+");
    }
    
    public static void order(){
    System.out.println("PRESS THE NUMBER OF THE ITEM YOU WANT TO BUY");
    System.out.print("Item Selected: ");
    choose = input.nextInt();
    
    //conditions
    if(choose==1){
        System.out.println("You selected Candy");
        System.out.print("How many Candy you want to buy? : ");
        quantity =input.nextInt();
        total = total +(quantity*15);
        
            System.out.println("Total cost of item/s selected: " + quantity*15);
            System.out.println("Enter your payment ");
            pay = input.nextDouble();
            if(pay <=total){
              System.out.println("Sorry, your payment is not enough to continue this transaction");
              System.exit(0);
            }else{
            System.out.println("Here is your " +quantity + " Candy");
            System.out.println("Total price: " + total);
            total = pay-total;
            System.out.println("Change: " + total);
            System.out.println(" ");
            System.out.println("THANK YOU FOR BUYING!");
        }
    }else if(choose==2){
        System.out.println("You selected Chips");
        System.out.print("How many Chips you want to buy? : ");
        quantity =input.nextInt();
        total = total +(quantity*10);
        
        System.out.println("Total cost of item/s selected: " + quantity*10);
            System.out.println("Enter your payment ");
            pay = input.nextDouble();
            if(pay <=total){
              System.out.println("Sorry, your payment is not enough to continue this transaction");
              System.exit(0);
            }else{
            System.out.println("Here is your " +quantity + " Candy");
            System.out.println("Total price: " + total);
            total = pay-total;
            System.out.println("Change: " + total);
            System.out.println(" ");
            System.out.println("THANK YOU FOR BUYING!");
            }
      }else if(choose==3){
        System.out.println("You selected Gum");
        System.out.print("How many Gum you want to buy? : ");
        quantity =input.nextInt();
        total = total +(quantity*5);
        
        System.out.println("Total cost of item/s selected: " + quantity*5);
            System.out.println("Enter your payment ");
            pay = input.nextDouble();
            if(pay <=total){
              System.out.println("Sorry, your payment is not enough to continue this transaction");
              System.exit(0);
            }else{
            System.out.println("Here is your " +quantity + " Candy");
            System.out.println("Total price: " + total);
            total = pay-total;
            System.out.println("Change: " + total);
            System.out.println(" ");
            System.out.println("THANK YOU FOR BUYING!");
            }
      }else if(choose==4){
        System.out.println("You selected Cookies");
        System.out.print("How many Cookies you want to buy? : ");
        quantity =input.nextInt();
        total = total +(quantity*15);
        
        System.out.println("Total cost of item/s selected: " + quantity*15);
            System.out.println("Enter your payment ");
            pay = input.nextDouble();
            if(pay <=total){
              System.out.println("Sorry, your payment is not enough to continue this transaction");
              System.exit(0);
            }else{
            System.out.println("Here is your " +quantity + " Candy");
            System.out.println("Total price: " + total);
            total = pay-total;
            System.out.println("Change: " + total);
            System.out.println(" ");
            System.out.println("THANK YOU FOR BUYING!");
            }
    }else if(choose==5){
        System.out.println("THANK YOU FOR BUYING!");
        System.exit(0);
    }else{
        System.out.println("Choose 1 to 5 only!");
        order();
    }
    }
    public static void main(String[] args) {
       menu();
       order();
    }
}
