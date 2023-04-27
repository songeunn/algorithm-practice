# Map 활용

**❓ Map의 메서드**

* `new Map()` : 맵 생성
* `map.set(key, value)` : key와 value 저장
* `map.get(key)` : key에 해당하는 값 반환 (없을 경우 undefined)
* `map.has(key)` : key의 존재여부 boolean으로 반환
* `map.delete(key)` : key와 해당하는 값 삭제
* `map.clear()` : 맵 안의 모든 요소 제거
* `map.size` : 요소의 개수 반환



{% code title="예시" %}
```javascript
const db = [["programmer02", "111111"], ["programmer00", "134"], ["programmer01", "1145"]];
const map = new Map(db);
console.log(map);
/*
Map(3) {
  'programmer02' => '111111',
  'programmer00' => '134',
  'programmer01' => '1145'
}
*/
map.has('programmer01') // true
map.get('programmer01') // 1145
```
{% endcode %}
