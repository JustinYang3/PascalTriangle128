# PascalTriangle128
import java.util.Scanner;
public class main {

	public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        System.out.println("Enter the amount of lines wanted of Pascal's Triangle: ");
        int num = scan.nextInt();
        
        int[][] array=new int[num][num];
        for (int i = 0; i < num; i++)
        {
            for(int j = 0; j <= i; j++)
            {
                if(j == 0 || j == i)
                    array[i][j] = 1;
                else
                    array[i][j] = array[i-1][j] + array[i-1][j-1];
                
            }
        }
        for (int i = 0; i < num; i++)
        {
            for (int j = 0; j < num - i; j++)
                System.out.print(" ");
            for (int k = 0; k <=i; k++)
                System.out.print(array[i][k]+" ");
            System.out.println();
        }
    }
    
}
