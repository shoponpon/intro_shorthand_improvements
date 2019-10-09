@title[Introduction of Shorthand Property Assignment Improvements]

##### state 0
### Shorthand<br/>Property Assignment<br/>Improvements
##### 2019.10.09 \#tc_study38

###### Proposal: [https://github.com/rbuckton/proposal-shorthand-improvements](https://github.com/rbuckton/proposal-shorthand-improvements)

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
```JavaScript
const a = {x: o.x};
```

<br/>

#### Proposal
```JavaScript
const a = {o.x};
```

+++
@snap[north raleway-medium span-80]
### Initialize(bracket notation)
@snapend

#### Current
```JavaScript
const a = {'x': o['x']};
```

<br/>

#### Proposal
```JavaScript
const a = {o['x']};
```

---
@snap[north raleway-medium span-80]
### Destruct(dot notation)
@snapend

#### Current
```JavaScript
({ x: a.x } = o);
```

<br/>

#### Proposal
```JavaScript
({ a.x } = o);
```

+++
@snap[north raleway-medium span-80]
### Destruct(dot notation)
@snapend

#### Current
```JavaScript
({ 'x': a['x'] } = o);
```

<br/>

#### Proposal
```JavaScript
({ a['x'] } = o);
```

---
code
```JavaScript
var o = {foo: 123, bar: true, 'poyo': null};
var a = {};
({foo: a.foo, bar: a.bar, 'poyo': a['poyo']} = o);

console.log(a);
```
@[3]

stdout
```JavaScript
{ foo: 123, bar: true, poyo: null }
```

+++
code
```JavaScript
var o = {foo: 123, bar: true, 'poyo': null};
var a = {};
({a.foo, a.bar, a['poyo']} = o);

console.log(a);
```
@[3]

stdout
```JavaScript
{ foo: 123, bar: true, poyo: null }
```

---
# スマート

---
# END
