# 문자열 내 p와 y의 개수

## 문제 링크

- https://school.programmers.co.kr/learn/courses/30/lessons/12916

## 나의 문제 풀이

1. p와 y의 갯수를 담을 변수를 0으로 초기화시킴
2. 주어진 문자열 s를 toLowerCase 메서드를 사용해서 소문자로 만듬
3. s 문자열에 대해서 for 반복문을 사용
4. p인 경우 +1을 해주고 y인 경우 -1을 해줌
5. 마지막에 num이 0인경우 true를 리턴하고 아닌 경우 false를 리턴함

```Js
function solution(s){
  let num = 0
  const lower = s.toLowerCase()
  
  for(let i=0;i<lower.length;i++){
    if(lower[i] === "p") num +=1
    else if(lower[i] === "y") num -= 1
  }
    
 return num === 0 ? true : false
}
```

## 다른 사람 풀이

1. 주어진 문자열 s를 대문자로 만든다.
2. split 메서드를 사용해 P를 잘라내고 length를 구한다.
3. 마찬가지로 split 으로 Y를 잘라내고 length를 구한다.
4. 2개를 비교해서 true or false를 리턴시킨다.

```Js
function numPY(s){
  return s.toUpperCase().split("P").length === s.toUpperCase().split("Y").length;
}
```

1. match 메서드와 정규표현식을 사용해서 p , y 의 갯수를 구하고 비교해서 리턴시킨다.

```Js
function numPY(s) {
  return s.match(/p/ig).length == s.match(/y/ig).length;
}
```

## 알게 된 점

- split 메서드를 사용해서 length를 비교하는 방법
- match(정규표현식)을 사용해서 비교하는 방법
