# x만큼 간격이 있는 n개의 숫자

## 문제 링크 

- https://school.programmers.co.kr/learn/courses/30/lessons/12954

## 문제 설명 

- 함수 solution은 정수 x와 자연수 n을 입력 받아, x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴해야 합니다. 

- 다음 제한 조건을 보고, 조건을 만족하는 함수, solution을 완성해주세요.

## 제한 사항

- x는 -10000000 이상, 10000000 이하인 정수입니다.
- n은 1000 이하인 자연수입니다.

## 나의 문제 풀이

1. 빈배열을 먼저 선언한다.
2. 반복문을 돌려서 배열에 넣는다.

```Js
function solution(x, n) {
  let answer = [];
  for (let i=1;i<=n;i++){
    answer.push(x*i)
  }
  return answer
}
```

## 다른 사람 풀이 

1. Array(n)으로 먼저 빈배열을 만든다
2. fill(x)로 만들 배열을 x로 채워 넣는다
3. map()을 사용해 각각 요소에 대해서 요소*인덱스+1를 한다.

```Js
function solution(x, n) {
    return Array(n).fill(x).map((v, index) => (index + 1) * v)
}
```
