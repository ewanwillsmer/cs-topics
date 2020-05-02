# Arrays Vs. Hashtables

Information coming from https://www.kirupa.com/html5/hashtables_vs_arrays.htm

Initially you would start with data:

| Name   | Age |
| ------ | --- |
| Ewan   | 28  |
| Anke   | 22  |
| Carla  | 22  |
| Xander | 29  |
| Sean   | 27  |

## Arrays

If you wanted to store your data in an array:

```javascript
var myData = [];

myData.push(["Ewan", "28"]);
myData.push(["Anke", "22"]);
myData.push(["Carla", "22"]);
myData.push(["Xander", "29"]);
myData.push(["Sean", "28"]);
```

If I was trying to find out Ewan's age:

```javascript
var person = "Ewan";

for (var i = 0; i < myData.length; i++) {
  if (myData[i][0] == person) {
    alert(person + "'s age is" + myData[i][1]);
  }
}
```

The loop goes through each item in the array checking to see if the myData[i][0] matches person. Once the item matches, we retrieve the corresponding myData[i][1].

## Hashtables

If you wanted to store the data in an Hashtables:

```javascript
var myData = {};

myData["Ewan"] = "28";
myData["Anke"] = "22";
myData["Carla"] = "22";
myData["Xander"] = "29";
myData["Sean"] = "27";
```

This time, if I was trying to find out Ewan's age I would only need to use

```javascript
var person = "Ewan";

alert(myData[person]);
```

Hashtables work by finding the exact location your value is stored and returning that value instantaneously or nearly instantaneously
