# [프로그래머스] k번째 수
``` java
import java.util.Arrays;
class Solution {
    public int[] solution(int[] array, int[][] commands) {
        int[] answer = new int[commands.length];

        for(int i = 0; i < commands.length; i++) {
            int one = commands[i][0];
            int two = commands[i][1];
            int three = commands[i][2];

            int[] copyArray = Arrays.copyOfRange(array, one-1, two);
            Arrays.sort(copyArray);

            answer[i] = copyArray[three-1];
        }

        return answer;
    }
}
```

### length와 length()의 차이(feat. size())
> length : 배열의 길이
* 
> length() : 문자열의 길이
* 
> size() : 컬렉션프임워크 타입의 길이
*

### Arrays 클래스와 메소드(import java.util.Arrays)
``` java
    int[] arr = {2, 4, 5, 3, 1, 7 ,6};
```
> Arrays.copyOf(원본배열, end)
``` java
    Arrays.copyOf(arr, 5);
    //{2, 4, 5, 3, 1, 7}
```
> Arrays.copyOfRange(원본배열, start, end)
``` java
    Arrays.copyOfRange(arr, 1, 3);
    //{2, 4, 5, 3}
```
> Arrays.sort()
``` java

```

### 2차원 배열의 길이 구하기
``` java
    String[][] arr = {{"A","B","C"} 
                    , {"D","E"}
                    , {"F","G","H","I"}};
```
> row(행) : 2차원 배열의 row 수
``` java
    arr.lenth; //3
```
> column(열) : 각 row의 column 수
``` java
    arr[0].lenth; //3
    arr[1].lenth; //2
    arr[2].lenth; //4
```
