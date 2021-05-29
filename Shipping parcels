import java.io.*; // for handling input/output
import java.util.*; // contains Collections framework

// don't change the name of this class
// you can add inner classes if needed
class Main {
	public static void main (String[] args) {
                      // Your code here
					  Scanner inp = new Scanner(System.in);
					  int t = inp.nextInt();
					  for (int i=0;i<t;i++){
						  int n = inp.nextInt();
						  int d = inp.nextInt();
						  int [] weight = new int[n];
						  for (int j=0;j<n;j++){
							  weight[j] = inp.nextInt();
						  }
						  //System.out.println(weight[0]);
						  System.out.println(findWtCapacity(weight,n,d));
					  }
					  
	}
	public static int findWtCapacity(int weights[], int n, int D){
		int low=0, high = 0;
		for (int i=0;i<n;i++){
			low = Math.max(low,weights[i]);
			high+=weights[i];
		}
		while (low<high){
			int midWC = low + ((high-low)/2);
			if(numOfDays(midWC, weights, n)>D){
				low = midWC+1;
			}else{
				high = midWC;
			}
		}
		return low;
	}
	public static int numOfDays(int wc, int weights[], int n){
		int days = 0;
		int sumOfParcelsTillNow = 0;
		for (int i=0;i<n;i++){
			if (sumOfParcelsTillNow + weights[i] <= wc){
				sumOfParcelsTillNow += weights[i];
			}else{
				days++;
				sumOfParcelsTillNow = weights[i];
			}
		}
		if (sumOfParcelsTillNow>0){
			days++;
		}
		return days;
	}
}
