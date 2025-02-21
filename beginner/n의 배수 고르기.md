## 문제 링크

https://school.programmers.co.kr/learn/courses/30/lessons/120905

---

## 문제 설명

정수 n과 정수 배열 numlist가 매개변수로 주어질 때, numlist에서 n의 배수가 아닌 수들을 제거한 배열을 return하도록 solution 함수를 완성해주세요.

---

## 입출력 예 설명

입출력 예 #1 : numlist에서 3의 배수만을 남긴 [6, 9, 12]를 return합니다.

입출력 예 #2 : numlist에서 5의 배수만을 남긴 [10, 5]를 return합니다.

입출력 예 #3 : numlist에서 12의 배수만을 남긴 [120, 600, 12, 12]를 return합니다.

---

## 풀이

```java
import java.util.List;
import java.util.ArrayList;

class Solution {
    public int[] solution(int n, int[] numlist) {
        List<Integer> answer = new ArrayList();
        for (int i : numlist) {
            if (i % n == 0) {
                answer.add(i);
            }
        }
        return answer.stream().mapToInt(Integer::intValue).toArray();
    }
}
```

---

## 좋아요 최다 풀이

```java
import java.util.Arrays;

class Solution {
    public int[] solution(int n, int[] numList) {
        return Arrays.stream(numList).filter(value -> value % n == 0).toArray();
    }
}
```
