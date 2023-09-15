# 삽입 정렬(Insert Sort)
---
<br>

  **For example**
  ```java
  package Altest;
  
  import java.util.Scanner;
  import java.util.Arrays;
  
  
  public class InsertSort {
	
  	public static void main(String[] args) {
  		int[] arr = new int[10];
  		int j;
  		
  		Scanner sc = new Scanner(System.in);
  		for (int i = 0; i < arr.length; i++) {
  			System.out.print(i+1 + "번째 변수 입력 :");
  			arr[i] = sc.nextInt();	
  		}
  		System.out.println(Arrays.toString(arr));
  		
  		
  		for(j = 1; j < arr.length; j++) { 
  		//for(j = 1; j < 10; j++){
  		   int temp = arr[j];
  		   int prev = j - 1;								// j가 1일 때 prev 0
  		   while((prev >= 0) && (arr[prev] > temp)) {		// prev자리 값이 temp 보다 크고 prev가 음수가 아닐 경우
  		      arr[prev+1] = arr[prev];						// prev자리 값을 prev+1 자리에 대입
  		      prev--;										// prev이전 자리 값으로 변경 후 루프.
  		   }
  		   arr[prev + 1] = temp;
  		}
  		System.out.println(Arrays.toString(arr));

	  }
  }
  ```
