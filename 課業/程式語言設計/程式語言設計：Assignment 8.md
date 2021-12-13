# Programming Language Design Assignment #7

To TA:
這是MD檔匯出的格式，Code絕非截圖

## Logging
No
因為藉由`within(Logging)` 我們可以抓到是不是在一個aspect裡面執行的`println()` 如果是的話，就不會再執行`after()`，換句話說，就是不會被aspect給抓到

## Memorization
```Java
public aspect Cache{
	static private int CACHE_SIZE = 33;
	private int[][] cache 
		= new int[CACHE_SIZE][CACHE_SIZE];
	
	pointcut binoCall(int n, int k):
		call(int Bin.binomail(int, int)) 
			&& args(n) && args(k);
	
	int around(int n, int k) binoCall(n) {
		int value = 0;
		if(n < CACHE_SIZE && k < CACHE_SIZE) {
			value = cache[n][k];
		}
		if(value > 0) {
			return value;
		}
		value = proceed(n, k);
		if(n < CACHE_SIZE && k < CACHE_SIZE) {
			cache[n][k] = value;
		}
		return value;
	}
}
```