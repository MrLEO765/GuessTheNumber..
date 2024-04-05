# GuessTheNumber..
import java.util.*;
public class GuessTheNum {
   public static void main(String[] args) {
    
        Scanner sc  = new Scanner (System.in);
        Random num = new Random();
        char PlayAgain;
       do{

        
        char choose ;
        int tryCounts = 0;
    System.out.println( "Choose the level:- 1.Easy 2.Medium 3.Hard " + "\nSelect an Numeber:" );
    choose = sc.next().charAt(0);
    
          switch (choose) {
            case '1':
           
            System.out.println("You have Entered in Easy Mode: ");
            int RandomNum = num.nextInt(100)+1;
                System.out.println("You only got 10 trials....  \nGuees the Number Between (1-100): ");
                while (true) {

               int playerGuess = sc.nextInt();
                 tryCounts++;
                  if(tryCounts >= 10){
    System.out.println("Losser! You have exhausted your 10 trials  " +"   "+ "\nThe Answer is:"+" "+ RandomNum);      
              break;
                      }
                  if(RandomNum == playerGuess){
                      
                   System.out.println("Hurray!"+" "+"Winner Winner Chicken Dinner!");
                   System.out.println("It tooks you :"+ tryCounts +" "+"Gussese");
                   break;
           
                  }else if( RandomNum < playerGuess){
           
                   System.out.println("Number is lesser");
           
                  }else{
                   System.out.println("Number is Greater");
                       }                
                }
                break;
            case'2':
            
            System.out.println("You have Entered in Medium Mode: ");
            int RandomNum2 = num.nextInt(250)+1;

                System.out.println("You only got 7 trials....  \nGuees the Number Between (1-250): ");
                while (true) {

               int playerGuess2 = sc.nextInt();
                 tryCounts++;
                  if(tryCounts >= 7){
  System.out.println("Losser! You have exhausted your 7 trials   " +"   "+ "\nThe Answer is:"+" "+ RandomNum2);
                  break; 
                  }
                  if(RandomNum2 == playerGuess2){
                      
                   System.out.println("Hurray!"+" "+"Winner Winner Chicken Dinner!");
                   System.out.println("It tooks you :"+ tryCounts +" "+"Gueeses");
                   
                   break;
           
                  }else if( RandomNum2 < playerGuess2){
           
                   System.out.println("Number is lesser");
           
                  }else{
                   System.out.println("Number is Greater");
                       }
                    }
                break;
            case'3':
            
            System.out.println("You have Entered in Hard Mode: ");
            int RandomNum3 = num.nextInt(500)+1;
                System.out.println("You only have 5 trials.... \nGuees the Number Between (1-500): ");
                while (true) {
               int playerGuess3 = sc.nextInt();
                 tryCounts++;
                  if(tryCounts >= 5){
     System.out.println("Losser! You have exhausted your 5 trials  " +"   "+ "The Answer is:"+" "+ RandomNum3);
     break;
    }     
       
                  if(RandomNum3 == playerGuess3){
                      
                   System.out.println("Hurray!"+" "+"Winner Winner Chicken Dinner!");
                   System.out.println("It tooks you :"+ tryCounts +" "+"Guesses");
                   break;
           
                  }else if( RandomNum3 < playerGuess3){
           
                   System.out.println("Number is lesser");
           
                  }else{
                   System.out.println("Number is Greater");
                    }
                }
                 break;

            default:
                  System.out.println("Noob! Try again....");
                    }        
                
           
        System.out.println("Do you wanted to play again?  (Y/N)");
       PlayAgain = sc.next().charAt(0);
                }while (PlayAgain == 'Y' && PlayAgain == 'y');
      System.out.println(" Thank you for Playing.... Goodbye!");
         
       }
    }

