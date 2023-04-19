# 배열 중복값 제거하기

## Set

```javascript
const dupArr = [1, 2, 3, 1, 2];
const set = new Set(dupArr);
const uniqueArr = [...set];

console.log(uniqueArr);
// [1, 2, 3]
```

* `const set = new Set(dupArr)` : 중복값이 있는 배열을 Set 객체로 만들어서 중복을 제거한다.
* `const uniqueArr = [...set]` : spread 연산자를 사용하여 Set 객체를 다시 배열로 변환한다. Set 객체를 배열로 변환할 때 spread 연산자 대신, `Array.from()` 또는 `forEach()` 문을 사용할 수도 있다.

```javascript
const arr = [1, 2, 3, 1, 2];
const unique = [...new Set(arr)]; // 👉한줄로 깔끔하게
console.log(unique); // [1, 2, 3];
```



## forEach(), inclues()

```javascript
const dupArr = [1, 2, 3, 1, 2];

let uniqueArr = [];
dupArr.forEach((element) => {
    if (!uniqueArr.includes(element)) {
        uniqueArr.push(element);
    }
});

console.log(uniqueArr);
// [1, 2, 3]
```

`forEach()` 함수로 주어진 배열을 순회하면서, 배열의 원소들로 주어진 callback 함수를 실행한다.

`include()` 함수는 주어진 배열에 특정값이 포함 여부를 검사한다.
