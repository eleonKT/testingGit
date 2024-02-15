# testingGit
This is my first time using GitHub so i'm gonna test it.

    /*
    We will check a simple exercise, the "Spider-man" sample.
    the exercise consists on count how many Spiderwebs he used for climb buildings (10),
    then he will stop on the greater building and counting it too.

    From 1 to 10, we're gonna use Integer numbers with this example: 4 5 5 7 12 6 7 6 5 4
    you can use Double numbers too: 4.2 5.2 5.5 7.6 12.5 6.4 7.8 6.5 5.9 4.1

    For Integer numbers example, the answer will be: 12 and 8
    For Double numbers example, its: 12.5 and 8.3
    */

    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {
            Double[] buildingHeight = new Double[10];
            double major, usedSpiderWebs=0;
            Scanner typing = new Scanner(System.in);

            System.out.print("Type the height of 10 buildings: ");
            for(int meter=0; meter<10; meter++){
                buildingHeight[meter] = typing.nextDouble();
            }

            major = buildingHeight[0];
            for(int meter=0; meter<buildingHeight.length; meter++){
                if(major<buildingHeight[meter]){
                    major = buildingHeight[meter];
                    usedSpiderWebs += (buildingHeight[meter] - buildingHeight[meter-1]);
                }
            }

            System.out.print("\nThe major buildingHeight is: "+major);
            System.out.println("\nThe amount of SpiderWebs used is: "+usedSpiderWebs);
        }
    }
