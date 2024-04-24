# graph
dsa
import java.util.Scanner;

/**
 * adjacnecy_matrix
 */
public class adjacnecy_matrix {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of Verteces:");
        int n = sc.nextInt();

        while (n<0) {
            System.out.println("Enter the valid Vertices : ");
            n = sc.nextInt();
        }

        int [][]arr = new int[n][n];

        for(int i = 0;i<n;i++){
            for(int j = 0;j<n;j++){
                System.out.println("Enter 1 if there is an edge between "+i+" and "+j+"else, enter 0");
                int edge = sc.nextInt();
                if(edge != 0 && edge != 1){
                    System.out.println("Enter the valid Edge : ");
                    edge = sc.nextInt();
                }
                arr[i][j] = edge;
                arr[j][i] = edge;
            }
        }
        System.out.println("Printing the 2d Matrix: ");
        for(int i = 0;i<n;i++){
            for(int j= 0;j<n;j++){
                System.out.print(arr[i][j]+" ");
            }
            System.out.println();
        }

    }
}
