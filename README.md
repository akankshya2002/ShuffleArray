public class ShuffleArray {

	public static void main(String[] args) {
		Scanner s=new Scanner(System.in);
		System.out.println("Enter the number of elements you want to store");
		int n=s.nextInt();
		int[] arr=new int[n];
		System.out.println("Enter the elements to enter");
		for(int i=0; i<n; i++)  
		{ 
			arr[i]=s.nextInt();  
		}  
		System.out.println("Array elements are: ");  
		Random ran=new Random();
		for (int i = 0; i < arr.length; i++)
		{
			int randomIndexToSwap = ran.nextInt(arr.length);
			int temp = arr[randomIndexToSwap];
			arr[randomIndexToSwap] = arr[i];
			arr[i] = temp;
		}
		System.out.println(Arrays.toString(arr));
	}
		
	}
