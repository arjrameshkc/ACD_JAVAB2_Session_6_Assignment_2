# ACD_JAVAB2_Session_6_Assignment_2
package Session6_Assignment;

public class PrimeNumber implements Runnable{
	int n,m,i,flag=0;
	
	public PrimeNumber(int n){
		super();
		this.n = n;
		
	}	

	@Override
	public void run() {
		// TODO Auto-generated method stub
		 m=n/2;
		
		 for(i=2;i<=m;n++)
	     {
	         if(n%i==0){
	        	 System.out.println("Number is not prime");  
	                 flag=1;
	                 break;
	         }
	      }
	         if(flag==0)
	             System.out.println(n+" Number is prime");
	     }
}


package Session6_Assignment;

import java.util.Scanner;

public class Mainprime {

		public static void main(String[] args) {
			// TODO Auto-generated method stub
			
			System.out.println("Enter the number which needs to be checked:");
			Scanner sc = new Scanner(System.in);
			int n = sc.nextInt();				  
			try
	        {
	            PrimeNumber p1= new PrimeNumber(n);
	            Thread t1=new Thread(p1);
	            t1.start();
	           
	        }
	        catch(Exception e1){	              
	       
		}

	}


}
