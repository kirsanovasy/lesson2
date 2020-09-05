# lesson2
package ru.geekbrains.lesson2;

import java.util.Arrays;

public class Main {

    public static void main(String[] args) {
/**
 * 1. Задать целочисленный массив, состоящий из элементов 0 и 1.
 * Например: [ 1, 1, 0, 0, 1, 0, 1, 1, 0, 0 ].
 * С помощью цикла и условия заменить 0 на 1, 1 на 0;
 */
        int[] array = {1, 1, 0, 0, 1, 0, 1, 1, 0, 0};
        System.out.println(Arrays.toString(array));
        changeArray(array);
        System.out.println(Arrays.toString(array));
        /**
         *  2. Задать пустой целочисленный массив размером 8.
         *  С помощью цикла заполнить его значениями 0 3 6 9 12 15 18 21;
         */
        int[] array2 = new int[8];
        System.out.println(Arrays.toString(array2));
        fillArray(array2);
        System.out.println(Arrays.toString(array2));
        /**
         * 3. Задать массив [ 1, 5, 3, 2, 11, 4, 5, 2, 4, 8, 9, 1 ]
         * пройти по нему циклом,
         * и числа меньшие 6 умножить на 2;
         */
        int[] array3 = {1, 5, 3, 2, 11, 4, 5, 2, 4, 8, 9, 1};
        System.out.println(Arrays.toString(array3));
        sixArray(array3);
        System.out.println(Arrays.toString(array3));
        /**
         * 4. Создать квадратный двумерный целочисленный массив (количество строк и столбцов одинаковое), и
         * с помощью цикла(-ов) заполнить его диагональные элементы единицами;
         */
        int[][] array4 = new int[10][10];
        printArray4(array4);

        diagonal(array4);
        System.out.println("");
        printArray4(array4);


    }

    public static void changeArray(int[] inputArray) {
        for (int i = 0; i < inputArray.length; i++) {
            inputArray[i] = 1 - inputArray[i];
        }
    }

    public static void fillArray(int[] inputArray) {
        for (int i = 0; i < inputArray.length; i++) {
            inputArray[i] = i * 3;
        }
    }

    public static void sixArray(int[] inputArray) {
        for (int i = 0; i < inputArray.length; i++) {
            inputArray[i] = (inputArray[i] < 6) ? (inputArray[i] * 2) : (inputArray[i]);
        }
    }

    static void printArray4(int[][] inputArray) {
        for (int i = 0; i < inputArray.length; i++) {
            System.out.println(Arrays.toString(inputArray[i]));
        }
    }
    static void diagonal(int[][]  array){
        for (int i = 0; i < array.length; i++)
        {
            array[i][i] = 1;
            array[i][ array[i].length - 1 - i] = 1;
        }

    }
}
