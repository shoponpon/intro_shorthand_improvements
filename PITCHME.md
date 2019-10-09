@title[Introduction of Shorthand Property Assignment Improvements]

##### state 0
### Shorthand<br/>Property Assignment<br/>Improvements
##### 2019.10.09 \#tc_study38

---
@snap[north raleway-medium span-80]
#### 概要
@snapend

### プロパティ割り当ての<br/>省略記法の提案
 - オブジェクトのInitialize |
 - オブジェクトのDestruct | 

---
@snap[north raleway-medium span-80]
## Initialize(dot notation)
@snapend

### Current
```text
const a = {x: o.x};
```

<br/>

### Proposal
```text
const a = {o.x};
```

+++
@snap[north raleway-medium span-80]
## Initialize(bracket notation)
@snapend

### Current
```text
const a = {'x': o['x']};
```

<br/>

### Proposal
```text
const a = {o['x']};
```

---
@snap[north raleway-medium span-80]
## Destruct(dot notation)
@snapend

### Current
```text
({ x: a.x } = o);
```

<br/>

### Proposal
```text
({ a.x } = o);
```

+++
@snap[north raleway-medium span-80]
## Destruct(dot notation)
@snapend

### Current
```text
({ 'x': a['x'] } = o);
```

<br/>

### Proposal
```text
({ a['x'] } = o);
```

---

---
@snap[north raleway-medium span-80]
## お気持ち
@snapend
```text
({ a.x } = o);
```

これちょっとわかりにくいかもしれない。

```text
({ x: a.x } = o); //期待される動作
a.x = o.x; // これと混同しそう
```

---
# END
