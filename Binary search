static int isPresent(long arr[], int n, long k)
{
	    // Your code here
		return search(arr,0,n-1,k);
}
public static int search(long arr[], int l, int r, long k){
	if (l<=r){
		int m = l+((r-l)/2);
		if (arr[m]==k){
			return 1;
		}else if (arr[m]>k){
			return search(arr,l,m-1,k);
		}else{
			return search(arr,m+1,r,k);
		}
	}
	return -1;
}
