## 04.29 배열  d - day 만들기

```java
public class quiz04 {
	public static void main(String[] args) {
		int[] dates = { 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31 };
		int goal = 0;
		Scanner sc = new Scanner(System.in);

		System.out.println("목표월");
		int mon = sc.nextInt();
		System.err.println("목표일");
		int day = sc.nextInt();

		for (int index = 0; index < mon - 1; ++index) {
			goal += dates[index];
		}  // 1월 1일 부터 목표달까지

		System.out.println(goal + day - 1);

		int passday = 0;
		System.out.println("시작월");
		int smon = sc.nextInt();
		System.out.println("시작일");
		int sday = sc.nextInt();

		for (int index = 0; index < smon - 1; ++index) {
			passday += dates[index];
		}

		System.out.println((goal + day) - (passday + sday));

	}// 시작 일 부터 목표 일까지

}
```

