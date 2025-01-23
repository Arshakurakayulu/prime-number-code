# prime-number-code

import java.util.Scanner;
public class Main
{
    public static int alt(int n){
        int sum=0;
        int count=0;
        for(int i=2;i<n*3;i++){
            boolean isprime=true;
            for(int j=2;j<=i/2;j++ ){
                if(i%j==0){
                    isprime=false;
                    break;
                }
            }
                if(isprime){
                    count++;
                    System.out.print(i+" ");
                   sum=sum+i;
                }
                if(count==n){
                    break;
                }
            
        }
        return sum;
    }
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		System.out.println(alt(n));
		
	}		
}
