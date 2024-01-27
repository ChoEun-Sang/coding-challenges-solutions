## <a href='https://school.programmers.co.kr/learn/courses/30/lessons/42748'>K번째수</a>

```javascript
function solution(array, commands) {
  return commands.map(
    ([i, j, k]) => array.slice(i - 1, j).sort((a, b) => a - b)[k - 1]
  );
}
```
