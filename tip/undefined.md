# 배열 생성 및 채우기

### 하나의 수로 배열 채우기

```javascript
let n = 15;
let arr = new Array(n).fill(0);
console.log(arr) // [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]
```

### 1부터 정해진 수까지 채우기

```javascript
let n = 15;
let arr = Array.from(new Array(n), (x, i) => i + 1);
console.log(arr) // [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
```

### 0부터 정해진 수까지 채우기

```javascript
let n = 15;
let arr = Array.from(Array(n).keys());
console.log(arr); // [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14]
```

```javascript
let n = 15;
let arr = [...Array(n)].map((x, i) => i);
console.log(arr); // [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14]
```
