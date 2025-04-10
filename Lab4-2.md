# Lab-4-K-200
import java.util.Scanner;
import java.util.Random;

public class MatrixMinMaxSwap {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random rand = new Random();

        System.out.print("Введіть кількість рядків: ");
        int rows = scanner.nextInt();
        System.out.print("Введіть кількість стовпців: ");
        int cols = scanner.nextInt();

        double[][] matrix = new double[rows][cols];


        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = -100 + rand.nextDouble() * 200;
            }
        }

        System.out.println("\nПочаткова матриця:");
        printMatrix(matrix);

        
        int minRow = 0, minCol = 0;
        int maxRow = 0, maxCol = 0;
        double min = matrix[0][0];
        double max = matrix[0][0];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (matrix[i][j] < min) {
                    min = matrix[i][j];
                    minRow = i;
                    minCol = j;
                }
                if (matrix[i][j] > max) {
                    max = matrix[i][j];
                    maxRow = i;
                    maxCol = j;
                }
            }
        }
