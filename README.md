# javascript

## Spread syntax (...)
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax

```javascript

var person = {
    name: "Ahoj",
    date: "asdf"
}

var entity = {
    age: 6
}

var p = {
    ...person,
    ...entity
}

```

```typescript
const subItems: { [key: string]: number } = {};
subItems["a"] = 1;
console.log(Object.keys(subItems).length);
```


```typescript
class Person {
    name: string;
    place: string;

    constructor(i: string, p: string) {
        this.name = i;
        this.place = p;
    }
}

function getPropertyValue(j: any, name: string): string {
    return j[name];
}

var arr: Person[] = [];
arr = [new Person("a", "1"), new Person("c", "3"), new Person("b", "2"), new Person("x", "100")];

function sortedArray(arr: any[], propertyName: string): any[] {
    return arr.sort((a, b) => {
        const aV = getPropertyValue(a, propertyName);
        const bV = getPropertyValue(b, propertyName);

        if (aV > bV) {
            return 1;
        } else {
            return -1;
        }
    });
}

console.log(sortedArray(arr, "name"));
```

```javascript
class Person {
    constructor(i, p) {
        this.name = i;
        this.place = p;
    }
}
function getPropertyValue(j, name) {
    return j[name];
}
var arr = [];
arr = [new Person("a", "1"), new Person("c", "3"), new Person("b", "2"), new Person("x", "100")];
function sortedArray(arr, propertyName) {
    return arr.sort((a, b) => {
        const aV = getPropertyValue(a, propertyName);
        const bV = getPropertyValue(b, propertyName);
        if (aV > bV) {
            return 1;
        }
        else {
            return -1;
        }
    });
}
console.log(sortedArray(arr, "name"));
```
