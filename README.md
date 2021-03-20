# learning-JS
learning JavaScript

main content here.

```js
/**
 * Create a House object.
 */

const House = {
  name: "Aydin's Sweet Home",
  Area: 63,
  color: "white",
  Rooms: 3,
  bedRoom: {
    Shelf: 2,
    Table: 1,
  },
  windowOpen: false,
  toggleWindow: function (windowStatus) {
    this.windowOpen = windowStatus;
  },
  newbedRoom: function (newbedRoomShelf, newbedRoomTable) {
    this.bedRoom.Shelf = newbedRoomShelf;
    this.bedRoom.Table = newbedRoomTable;
  },
};

console.log("The House Info:", House);
```
![image](https://user-images.githubusercontent.com/49828191/111854945-661cf800-8922-11eb-8305-978863e2c297.png)



```js
console.log("The House Name:", House.name);
console.log("The House Rooms:", House.Rooms);

console.log("The Shelf value before:", House.bedRoom.Shelf);

House.newbedRoom(5, 4);
console.log("The Shelf value after:", House.bedRoom.Shelf);
```
![image](https://user-images.githubusercontent.com/49828191/111855001-9cf30e00-8922-11eb-99c4-4368096ca192.png)

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
