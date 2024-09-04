import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size");
        int N = sc.nextInt();
        System.out.println("Enter k");
        int k = sc.nextInt();
        int[] arr = new int[N];
        for(int i=0; i<N; i++){
            System.out.println("Enter student"+i);
            arr[i] = sc.nextInt();
        }
        for(int i=1; i<=k; i++){
            System.out.println("Enter X");
            int x = sc.nextInt();
            System.out.println("Enter Y");
            int y = sc.nextInt();
            System.out.println("Result for reevaluation "+i+" is "+fun(x,y,arr));
        }
    }
        public static int fun(int x, int y, int[] arr){
            arr[x-1]  = y;
            int ans = 1;
            for(int i=1; i<arr.length; i++){
                if(arr[i]!=arr[i-1]){
                    ans+=1;
                }
            }
           return ans;
        }
}
        
