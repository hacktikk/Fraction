# Fraction
import java.util.*;
public class Hello {

    public static void main(String[] args) {
		//Your Code Here
		Scanner sc= new Scanner(System.in);
		String s=sc.next();
		int m=0;
		String s1[]=s.split("/");
		int s2[]= new int[s1.length];
		for(int i=0;i<s1.length;i++) {
		 s2[i]=Integer.parseInt(s1[i]);
		}
		if(s2[0]>s2[1]) {
		    m=s2[0];
		}
		else {
		    m=s2[1];
		}
		for(int i=2;i<=m/2;i++) {
		    if(s2[1]%i==0&&s2[0]%i==0) {
		        s2[0]=s2[0]/i;
		        s2[1]=s2[1]/i;
		    }
		}
 		System.out.print(s2[0]+"/"+s2[1]);

	}
}
