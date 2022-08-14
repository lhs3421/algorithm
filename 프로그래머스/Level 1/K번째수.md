# K번째수

## 문제 링크

- https://school.programmers.co.kr/learn/courses/30/lessons/42748

## 나의 문제 풀이

1. result 변수를 선언해서 빈배열로 초기화시킴
2. for 반복문을 0부터 commands의 길이까지 돌고 i를 1씩 증가시킴
3. slice를 이용해서 주어진 조건에 따라서 잘라내고 sort메서드를 사용해서 오름차순으로 정렬시킴
4. result에 정렬된 배열의 필요한인덱스에 -1을 해서 푸쉬해줌
5. result를 리턴함

```Js
function solution(array,commands) {
  let result = [];
  for(let i=0;i<commands.length;i++){
    const sort = array.slice(commands[i][0]-1,commands[i][1]).sort((a,b)=> a-b)
    result.push(sort[commands[i][2]-1])
  }
  return result
}
```

## 다른 사람 풀이

```Js
function solution(array, commands) {
    return commands.map(command => {
        const [sPosition, ePosition, position] = command
        const newArray = array
            .filter((value, fIndex) => fIndex >= sPosition - 1 && fIndex <= ePosition - 1)
            .sort((a,b) => a - b)    

        return newArray[position - 1]
    })
}
```

## 정리

```Js
const arr = [1,10,2,20,100]

console.log(arr.sort()) 
// [ 1, 10, 100, 2, 20 ]
console.log(arr.sort((a,b)=>a-b)) 
// [ 1, 2, 10, 20, 100 ]
```
