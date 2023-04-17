# 최소공배수(LCM) / 최대공약수(GCD)

## **유클리드 호제법을 이용한 풀이**

* a,b를 서로 나눌 때, 나누어진다면 b가 최대공약수이다. (a>b)
* 만약 a,b가 나누어지지 않으면 b와 a를 b로 나눈 나머지를 다시 나눈다.
* 서로가 나누어지면 a%b가 최대공약수이다. 나누어지지 않는다면 위처럼 b와 a를 b를 나눈 나머지를 다시 나눈다.

```js
function solution(n, m) {
    const gcd = (a, b) => a % b === 0 ? b : gcd(b, a % b);
    const lcm = (a, b) => a * b / gcd(a, b);
    return `최대공약수 ${gcd(n, m)}, 최소공배수 ${lcm(n, m)}`
}

console.log(solution(3, 15));
```
