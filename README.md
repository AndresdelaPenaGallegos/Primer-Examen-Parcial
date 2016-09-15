# Primer-Examen-Parcial
Running Time of Algorithms (java 7) 

Andres de la Pena Gallegos
148213
Fecha de entrega: 16/09/2016

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int size = sc.nextInt();
        int t=0;
        int contador = 0;
        int[] list = new int[size];
        for( int i = 0; i<size; i++)
            {
            list[i] = sc.nextInt();
        }
        for(int i= 0; i < list.length - 1; i++)
            {
            for(int j = i;j>=0 && list[j+1] < list[j];j--)
                {
                if(list[j+1] < list[j])
                    {
                    t = list[j+1];
                    list[j+1] = list[j];
                    list[j]=t;
                    contador= contador +1;
                }
                
            }
        }
        System.out.println(contador);
        
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
    }
}
