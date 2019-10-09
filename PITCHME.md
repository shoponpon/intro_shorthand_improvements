##### state 0
#### Shorthand Property Assignment Improvements
##### 2019.10.09 \#tc_study38

---
@snap[north raleway-medium span-80]
#### 概要
@snapend

### プロパティ割り当ての省略記法の提案
#### - オブジェクトのInitialize
#### - オブジェクトのDestruct

---
@snap[north raleway-medium span-80]
### Initialize
@snapend

## Current
```text
const a = {x: o.x};
```

<br/>

## Proposal
```text
const a = {o.x};
```

---

@snap[north raleway-medium span-80]
### Destruct
@snapend

## Current
```text
({ x: a.x } = o);
```

<br/>

## Proposal
```text
({ a.x } = o);
```
---
