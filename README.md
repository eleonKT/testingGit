# testingGit
This is my first time using GitHub so i'm gonna test it.

/*
    We will check a simple exercise, the "Spider-man" sample.
    the exercise consists on count how many Spiderwebs he used for climb buildings (10),
    then he will stop on the greater building and counting it too.

    From 1 to 10, we're gonna use Integer numbers with this example: 4 5 5 7 12 6 7 6 5 4
    For this first example, we'll count only major building.
 */

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Double[] buildingHeight = new Double[10];
        double major;
        Scanner typing = new Scanner(System.in);

        System.out.print("Type the height of 10 buildings: ");
        for(int meter=0; meter<10; meter++){
            buildingHeight[meter] = typing.nextDouble();
        }

        major = buildingHeight[0];
        for(double meter : buildingHeight){
            if(major<meter){
                major = meter;
            }
        }

        System.out.print("\nmajor is: "+major+"\n");
    }
}
