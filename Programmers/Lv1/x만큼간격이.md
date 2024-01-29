## <a href='https://school.programmers.co.kr/learn/courses/30/lessons/12954'>x만큼 간격이 있는 n개의 숫자 </a>

```javascript
function solution(x, n) {
  return Array(n)
    .fill(x)
    .map((x, idx) => x * (idx + 1));
}

/**
 * 배열에 n개의 x를 만든 후
 * map 매서드로 각 요소에 각 인덱스만큼 x를 더한다
 */
```
