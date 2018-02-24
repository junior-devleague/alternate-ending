# alternate-ending

Which path will you take? Create an interactive story where readers choose a path down a unique story.

## Objective

Use **Objects**, **Arrays**, **If Statements** and **Click Handlers** to create this interactive story.

## Prerequisites

To complete this project, students should have the following:
* Basic understanding of HTML structures.
* Basic understanding of JavaScript and DOM (Variables, Functions, getElementById)

## Concepts

JS | Description
---| -----------
Array | A variable that can hold more than one value at a time. You can access these values by referring to an index number.
Object | A collection of properties. Properties are name value pairs. Resource: https://www.w3schools.com/js/js_objects.asp
boolean | True or false.

## Your Challenge

### Part I

To complete Part I, fulfill the following requirements:
1. Set up your project file structure through the command line.
2. Create the following:
* HTML file
* CSS file
* JS file
3. Link all of your files correctly.

---

### Part II HTML

To complete Part II, fulfill the following requirements:

1. Create the beginning story scene as you like. Make sure to have the following elements with ids in your HTML.
* image
* dialogue (can be a ```p``` element)
* 3 buttons
  * One button that will take readers through story A
  * One button that will take readers through story B
  * One button to go to the next panel (>)


### Part III CSS

To complete Part III, fulfill the following requirements:

1. Style your page as you like. Align items, provide margins, change the border-radius, add shadows, and more!

### Part IV JS

To complete Part IV, fulfill the following requirements:

1. Store the following in variables using ```document.getElementById``` like the example below:

``` javascript
var variableName = document.getElementById('id-goes-in-here');
```

* button A
* button B
* button next
* image
* dialogue

2. Create a variable called "counter" and set it equal to 0.

3. Create a variable called "trackABoolean" and set it equal to false. This will keep track if the user chose the A storyline or the B storyline.

4. Create an object for every panel, labelling it for the A or B storyline accordingly.

An object is a collection of properties. It is a variable that can hold other variables! Create the object to store the dialogue and image for each panel in your story like the example below.

``` javascript
var panel1A = {
  dialogue: "Once upon a time..",
  img: "http://wac.2f9ad.chicdn.net/802F9AD/u/joyent.wme/public/wme/assets/ec050984-7b81-11e6-96e0-8905cd656caf.jpg?v=30"
}
```

5. Create a variable called "trackA" to hold an array. In this array, store each of your panel objects for track A like so.

``` JavaScript
var trackA = [panel1A, panel2A, panel3A];
```

6. Create a variable called "trackB" to hold an array. In this array, store each of your panel objects for track B.

7. Create an onclick function on your button A as follows:

``` JavaScript
buttonA.onclick = function() {
// Put the rest of your code in here!
}
```

 * What happens when button A is clicked? We want to change the dialogue and the image source. How do we access our dialogue and image source from the array and using our counter? The example below is what you might do to change the dialogue:

``` javascript
dialogue.innerHTML = trackA[counter].dialogue;
```

  * Right now, counter is equal to 0. trackA[0] is the first element in the trackA array. This is the panel1A object! To access the dialogue, we can use object ("dot") notation. Setting it equal to the innerHTML of our dialogue box will allow our reader to see the next portion of our story.

  * Increment the counter by 1. This is so we can keep track of which panel we are on. We now are on the next panel.

  * Make button A and button B "disappear" and the next button "appear". Do this by changing the CSS display property in JavaScript. We can change CSS properties in JavaScript as follows:
  ``` javascript
  element.style.property = "value";
  ```
    * Change the ```display``` property of buttonA to "none".
    * Change the ```display``` property of buttonB to "none".
    * Change the ```display``` property of the next button to "inline".
  * Set the trackABoolean equal to true.

8. Create an onclick function for your button B. It will have the same code as the buttonA onclick function, except instead of trackA, you will be using trackB.

9. Create an onclick function for your next button. In this function, do the following:
  * Create an if statement that checks if trackABoolean is equal to true. If so, do the following:
    * Change the innerHTML of your dialogue container to that of the dialogue in the current panel for trackA. How do we know what the "current panel" is? Use the trackA array and the counter variable!
    * Change the image source to the image of the current panel for trackA.
  * If trackABoolean is NOT true, do the following:
    * Change the innerHTML of your dialogue container to that of the dialogue in the current panel for trackB.
    * Change the image source to the image of the current image panel for trackB.
  * Increment the counter so we know we are now in the next panel.

### Stretch Goals

1. Add sound and style your page so that readers have a one of a kind story experience!
