# P56_Vacation

import java.util.Scanner;

public class P56_Vacation {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        double rest = Double.parseDouble(scanner.nextLine());
        double restStotinki = rest * 100;
        int stotinkiAll = (int)(restStotinki);
        int leva = stotinkiAll / 100;
        int stotinki = stotinkiAll % 100;
        int countMoneti = 0;

        countMoneti += leva / 2 + leva % 2 +
                stotinki / 50 + stotinki % 50 / 20 +
                stotinki % 50 % 20 / 10 + stotinki % 50 % 20 % 10 / 5 +
                stotinki  % 50 % 20 % 10 % 5 / 2 + stotinki % 50 % 20 % 10 % 5 % 2;
        System.out.println(countMoneti);
    }
}
