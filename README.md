# ClimbingGrade.js

[![MIT License][license-image]][license-url]

> ClimbingGrade.js converts climbing grades between different systems.

Currently supported systems include: French, Australian, South African, UIAA, Hueco, Font, British, YDS

## Installation

With node:

```bash
npm install climbing-grade
```

For the browser:

```bash
bower install climbing-grade
```

```html
<script type="text/javascript" src="bower_components/climbing-grade/ClimbingGrade.js"></script>
```

or Minified
```html
<script type="text/javascript" src="bower_components/climbing-grade/ClimbingGrade.min.js"></script>
```

## Demo

[http://grantismo.github.io/ClimbingGrade.js/](http://grantismo.github.io/ClimbingGrade.js/)

## Usage

Format a given grade in other grading systems.


### Node

```javascript
var ClimbingGrade = require('climbing-grade'); 
var grade = new ClimbingGrade('9a', 'french');
grade.format('australian'); // '35'
grade.format('south_african'); // '37'
grade.format('uiaa'); // 'XI+'
grade.format('hueco'); // V12
grade.format('font'); // '8A+'
grade.format('british'); // 'E10 7c'
grade.format('yds'); // '5.14d'
```

### Browser

```html
<script type="text/javascript">
  var grade = new ClimbingGrade("9a", "french");
  alert(grade.format("yds"));
</script></script>
```

Supports ranges 

```javascript
var hueco = new ClimbingGrade('vb', 'hueco');
hueco.format('font'); // '1 to 3+'


var french = new ClimbingGrade('6c', 'french');
french.format('yds'); // '5.11a/5.11b'
```

### Systems

* 'french'
* 'australian'
* 'south_african'
* 'uiaa'
* 'hueco'
* 'font'
* 'british'
* 'yds'


## Tests

```bash
jasmine
```

## License

[MIT][license-url]

[license-image]: http://img.shields.io/badge/license-MIT-blue.svg?style=flat
[license-url]: LICENSE
