# DiceWithArrays

import java.util.Random;

public class DiceGame {
    public static void main(String[] args) {
        // Number of sets and throws
        int numofsets = 5;
        int numofthrows = 20;

        int[] highestnums = new int[numofsets];

        Random r = new Random();

        for (int i = 0; i < numofsets; i++) {
            int highestdice = 1; // The initial value 

            for (int j = 0; j < numofthrows; j++) {
                int dice = r.nextInt(6) + 1; // Generate a random number between 1-6

                if (dice > highestdice) {
                    highestdice = dice;
                }
            }

            highestnums[i] = highestdice;
        }

        // Her setten en yüksek zar değerini ekrana yazdır
        for (int i = 0; i < numofsets; i++) {
            System.out.println("The highest dice number in set " + (i+1) + " ==>> " + highestnums[i]);
        }
    }
}
