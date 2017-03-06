## Iteration loops (for and while)

> Loops are good for repetitive iterations or other repetitive tasks, like searching though lists, arrays etc 

#### For loops
> A **for** loop will run as long as the condition is true and we usually use a counter to make it run exactly the specified amount of times

Example

```javascript
for (let i = 0; i < 5; i++) {
    text += "The number is " + i + "<br>";
}
```
Or

```javacript
for (let i = 0, len = cars.length, text = ""; i < len; i++) { 
    console.log("Car number " + (i+1) + " is a " + cars[i]);
}
```
#### While loops
>The **while** loop loops through a block of code  a specified condition is true

Example

```javascript
while (i < 100) {
    text += "The number is not 100 yet, it's: " + i;
    i++;
}
```