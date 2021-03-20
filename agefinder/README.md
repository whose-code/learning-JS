### agefinder
```js
--index.html =>
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Classes</title>
    <script type="module" src="Agecalc.js"></script>
    <script type="module" src="script.js"></script>
  </head>
  <body></body>
</html>

--script.js =>
/**
 * Use the global Date() object to transform dates.
 * @link https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date
 */

import Agecalc from "./Agecalc.js";

const name1 = new Agecalc("Shaheer", "Male", "April 27, 1988");

console.log("Name:", name1.name);
console.log("Gender:", name1.gender);
console.log("Age:", name1.myAge());

--Agecalc.js =>
class Agecalc {
  constructor(name, gender, dateofBirth) {
    this.name = name;
    this.gender = gender;
    this.dateofBirth = dateofBirth;
  }
  myAge() {
    let now = new Date();
    // console.log("today:", now);
    let doB = new Date(this.dateofBirth);
    console.log("doB:", doB);
    let YearsGone = now - doB; // yearsgone time in milliseconds
    let currentAge = Math.floor(YearsGone / (1000 * 3600 * 24 * 31 * 12));
    return currentAge;
  }
}

export default Agecalc;
```
![image](https://user-images.githubusercontent.com/49828191/111856924-64f1c800-892e-11eb-910b-629a4ec576fe.png)
