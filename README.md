# learning-JS
learning JavaScript

main content here.

```
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



```
console.log("The House Name:", House.name);
console.log("The House Rooms:", House.Rooms);

console.log("The Shelf value before:", House.bedRoom.Shelf);

House.newbedRoom(5, 4);
console.log("The Shelf value after:", House.bedRoom.Shelf);
```
![image](https://user-images.githubusercontent.com/49828191/111855001-9cf30e00-8922-11eb-99c4-4368096ca192.png)

