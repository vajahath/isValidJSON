
![](https://raw.githubusercontent.com/vajahath/is-valid-json/master/media/logo.png)

##### Simple package to validate JSON files.


```javascript
isValidJSON('{"kity": "Fluffy"}'); // returns true
```



## Install / Update

```bash
npm install --save is-valid-json
```

## Usage

### Syntax

`isValidJSON(<argument>);`

### Example
```javascript
// load package
const isValidJSON = require('is-valid-json');

// use it
isValidJSON('{"this": "is","a": "good json"}') // -> returns parsed object: {"this": "is","a": "good json"}
isValidJSON({"this": "is","a": "good json"}) // -> returns same object

isValidJSON('{ha: "hi" meuo: "ho"}') // -> returns false
isValidJSON('[{"ths":asdf}{"adasd":asdf}]') // -> returns false

// empty arrays and objects
isValidJSON('[]') // -> returns false
isValidJSON('{}') // -> returns false
isValidJSON([]) // -> returns false
isValidJSON({}) // -> returns false
```

### Usage

**Syntax :** `b = isValidJSON(a);`

where `a` and `b` are as follows,

| value of `a`                           | value of `b`                  |
| -------------------------------------- | ----------------------------- |
| `null`                                 | `false`                       |
| `true` or `false`                      | `false`                       | 
| any number                             | `false`                       | 
| valid json as `string`                 | parsed json object            |
| valid json as `object`                 | same json object              |
| invalid json as `object`               | `false`                       |
| invalid json as `object`               | `false`                       |
| valid, but empty json                  | `false`                       |
| valid non-empty `object`               | same object                   |
| valid non-empty `array`                | same array                    |
| valid, but empty `object`              | `false`                       |
| valid, but empty `array`               | `false`                       |


<br>

### one more example

```javascript
isValidJSON('{"name": "Kitty", "friends":["tom", "jerry"]}');
/* returns the following parsed object:
    {
        name: "kitty",
        friends: ["tom", "jerry"]
    }
 */
```


If you wish to file any feature/bugs, mention it on [issues](https://github.com/vajahath/lme/issues).

<br>

Enjoy.

## Change log

 - v1.0.0
     - Initial release

## License
MIT &copy; [Vajahath Ahmed](https://mycolorpad.blogspot.in)