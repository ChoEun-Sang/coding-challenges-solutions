## <a href='https://school.programmers.co.kr/learn/courses/30/lessons/42747'>H-index</a>

```javascript
// 풀이 1
function solution(citations) {
  const sorted_array = citations.sort((a, b) => a - b);
  let n = sorted_array.length;
  let answer = 0;

  for (let i = 0; i < sorted_array.length; i++) {
    let HIndex = n - i;

    if (sorted_array[i] >= HIndex) {
      answer = HIndex;
      break;
    }
  }

  return answer;
}

// 풀이 2
function solution(citations) {
  const sortedCitations = citations.sort((a, b) => b - a); // 내림차순 정렬

  for (let h = 0; h < sortedCitations.length; h++) {
    if (sortedCitations[h] <= h + 1) {
      return h;
    }
  }

  return sortedCitations.length;
}
```
