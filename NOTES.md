Capturing these two methods of interaction from the README and moving them here:

### Stop & Jot
There's a ton of information we could record about the weather. Yet when you
read the weather report in the morning, all of that information is distilled
down to a handful of numbers: 34 degrees fahrenheit, 20% chance of
precipitation, 4 degree windchill...

Why do you think that might be?

When you take something complex and then hide that complexity under a more simple interface, you are using a technique called **abstraction**. 

From [wikipedia](https://en.wikipedia.org/wiki/Abstraction_(software_engineering)): In software engineering and computer science, abstraction is a technique for arranging complexity of computer systems. It works by establishing a level of complexity on which a person interacts with the system, suppressing the more complex details below the current level.

### Think-Pair-Share

<details>
<summary>How might abstraction be relevant as software developers? Take a
minute and discuss this with your squad.</summary>

We can use abstraction to represent real-world entities when we write software. This allows us to hide complex systems underneath easy to grasp objects and models. 
</details>


## Laptop abstraction and modeling 

jrhorn424 commented on May 18, 2016:

I really enjoyed @berziiii's presentation.

In particular, when demoing modeling a laptop, he scaffolded adding behavior like togglePower() and installSoftware() by defining these functions outside the object and referring to the previously created object literal inside the bodies of the function.
```js
let laptop = { /*...*/ };
const togglePower = function () {
  laptop.status === 'on' ? 'off' : 'on';
}
```
This gave us a chance to talk about encapsulation. We're hiding the "JavaScript" details of toggling power inside a well-named function that made sense in our domain.

Next, we noted our functions were related to our laptop but we had no way of knowing that from the source code. So, we could further encapsulate our behavior by adding it to the laptop itself.
```js
let laptop = { 
/* ... */
  togglePower: function () {
-    laptop.status === 'on' ? 'off' : 'on';
+    this.status === 'on' ? 'off' : 'on';
  }
};
```
And we were presented an opportunity to use this without explaining it (which is the domain of js-objects-this).

danman01 on 3/24/2017 writes: I did this talk for lm01, and have a few notes:

I did the code-along television section as a lab, and gave the squads more time to work on their television object, as well as attempt to run their code, call their methods and access the various attributes of the television.
I spent a good amount of time on javascript review during the Demo: Modeling in Javascript section when getting into the crayon code.

Since I spent more time on the JS review and on the TV lab, I did not have time for the final recipe website lab. The students worked on this during the workshop

To cut down on the time I spent, I would be more aware of how much time is spent on review, explanation of future topics like `this`, different ways to create and inspect JS objects, and tabling questions that aren't directly on topic.
