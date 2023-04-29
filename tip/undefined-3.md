---
description: toString, parseInt 활용
---

# 진수변환

### n진수 → 10진수 (parseInt)

```javascript
parseInt('변환시키고자하는 문자열', 해당수의 진수)
```

문자열을 특정 진수의 정수로 변환시킬 수 있다.

이 때 문자열을 변환하는 것이므로 **숫자여도 `''` 안에 삽입**해준다.

```javascript
let num = '11';
let parsing = parseInt(num, 2); // 2진수에서 10진수로
let parsing = parseInt(num, 8); // 8진수에서 10진수로
let parsing = parseInt(num, 16); // 16진수에서 10진수로
```



### 10진수 → n진수 (toString)

```javascript
10진수.toString(n진수)
```

10진수를 n진수로 변환시키고자 할 때 `toString`을 이용한다.

```javascript
let num = 3;
num.toString(2); // 11
```



### n진수 → n진수

```javascript
let binary = "1111111111";
let hex = parseInt(binary, 2).toString(16);	// 2진수에서 16진수로

let hex = "3ff";
let octal = parseInt(hex, 16).toString(8);	// 16진수에서 8진수로
```

n진수에서 10진수로 변환 후, 다시 원하는 n 진수로 변환
