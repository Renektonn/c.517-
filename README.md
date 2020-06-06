//c.517南南見島(其實是南南見鳥) 
package tem;
import java.util.Scanner;
public class Main { 
	public static void main(String[] args) {
		int [][]arr= {{0,1},{1,1},{8,8},{8,1},{1,8}}; //[0]:y [1]:x
		if(range(arr[0][0],arr[1][0],arr[2][0]) && range(arr[0][1],arr[1][1],arr[2][1])) {
			System.out.print(0);
		}
		else
			if(range(arr[0][0],arr[1][0],arr[2][0])) {
				small(absolutely(arr[0][1]-arr[1][1]),absolutely(arr[0][1]-arr[2][1]));
			}
		else	
			if(range(arr[0][1],arr[1][1],arr[2][1])){
				small(absolutely(arr[0][0]-arr[1][0]),absolutely(arr[0][1]-arr[2][0]));
			}
	}
	static boolean range(int n,int a,int b) { //判斷整數n是否在a到b之間
		if((a<=n && n<=b) || (b<=n && n<=a)) {
			return true;
		}
		return false;
	}
	static int absolutely(int n) {
		return n>0?n:-n;
	}
	static void small(int a,int b) {
		System.out.println(a<b?a:b);
	}
}
