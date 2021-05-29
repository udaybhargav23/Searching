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
						int k = inp.nextInt();
						int [] arr = new int[n];
						for (int j=0;j<n;j++){
							arr[j]=inp.nextInt();
						}
						Arrays.sort(arr);
						System.out.println(search(arr,k,arr[n-1]-arr[0]));
					  }
	}
	public static int search(int arr[], int k, int high){
		int low = arr[1]-arr[0];
		for(int i=0;i<arr.length-1;i++){
			low = Math.min(low,arr[i+1]-arr[i]);
		}
		while (low<high){
			int mid = low + ((high-low)/2);
			int count = check(arr,mid);
			if (count>=k){
				high = mid;
			}else{
				low = mid+1;;
			}
		}
		return low;
	}
	public static int check(int arr[], int mid){
		int count = 0, index;
		for (int i=0;i<arr.length-1;i++){
			index = binarySearch(arr, arr[i]+mid, 0, arr.length);
			count += index-i-1;
		}
		return count;
	}
	public static int binarySearch(int arr[], int diff, int low, int high){
		while (low<high){
            int mid = low + ((high-low)/2);
            if(diff >= arr[mid]){
                low = mid + 1;
			}else{
                high = mid;
			}
        }
    	return low;
	}
}
