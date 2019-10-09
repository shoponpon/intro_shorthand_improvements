@title[Introduction of Shorthand Property Assignment Improvements]

##### state 0
### Shorthand<br/>Property Assignment<br/>Improvements
##### 2019.10.09 \#tc_study38

---
@snap[north raleway-medium span-80]
### 概要
@snapend

### プロパティ割り当ての<br/>省略記法の提案
 - オブジェクトのInitialize |
 - オブジェクトのDestruct | 

---
@snap[north raleway-medium span-80]
### Initialize(dot notation)
@snapend

#### Current
```text
const a = {x: o.x};
```

<br/>

#### Proposal
```text
const a = {o.x};
```

+++
@snap[north raleway-medium span-80]
### Initialize(bracket notation)
@snapend

#### Current
```text
const a = {'x': o['x']};
```

<br/>

#### Proposal
```text
const a = {o['x']};
```

---
@snap[north raleway-medium span-80]
### Destruct(dot notation)
@snapend

#### Current
```text
({ x: a.x } = o);
```

<br/>

#### Proposal
```text
({ a.x } = o);
```

+++
@snap[north raleway-medium span-80]
### Destruct(dot notation)
@snapend

#### Current
```text
({ 'x': a['x'] } = o);
```

<br/>

#### Proposal
```text
({ a['x'] } = o);
```

---
code
```Text
var o = {foo: 123, bar: true, 'poyo': null};
var a = {};
@[2]({foo: a.foo, bar: a.bar, 'poyo': a['poyo']} = o);

console.log(a);
```

stdout
```
{ foo: 123, bar: true, poyo: null }
```

+++
code
```Text
var o = {foo: 123, bar: true, 'poyo': null};
var a = {};
@[2]({a.foo, a.bar, a['poyo']} = o);

console.log(a);
```

stdout
```
{ foo: 123, bar: true, poyo: null }
```

---
# END
