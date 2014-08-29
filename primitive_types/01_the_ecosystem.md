Primitive Types are the building blocks for everything we’ll make in Coffeescript!

## Numbers
Like all programming languages, we can use coffee script as a calculator; it defines functions that look like normal math.
so we can try
`56 * 5`

### Inspecting return values
When we're experimenting by running code entirely in the browser, when we want to see the value that our code returns, we have a few ways to see that from inside the browser itself.

`alert 65 * 5`
The first is to create an alert with the value returned from our code.

`console.log 65 * 5`
A less annoying option, especially if you’d like to see multiple  values, is to log the value to the javascript console. To see what’s logged there, open the console using the Chrome shortcut `Command` + `Option` + `J`.

(If you installed coffeescript on your computer, you can try all the expressions and see the return value directly in the Coffeescript REPL.)

### Assigning Variables
And we can assign the result of that expression to a variable. In Coffeescript and Javascript, the convention is to use camel case variable names, so instead of separating words by underscores like in Ruby, or dashes like in HTML class names, we just capitalize the beginning of the next word. But it’s important to lowercase the first word.

`numberOfConcernsIHaveAboutCoffeescript = 56 * 5`

## Booleans
We have booleans, true and false
`doesRachelCare = true`
`doesAdamCare = false`

You can also log multiple values to the console using a comma to separate the values.
`console.log “Does Rachel care? “, doesRachelCare`

## Strings
Like lots of other programming languages, you can use single quotes or double quotes.
`personTalkingTooMuch = “Rachel”`
`bestListener = “Liskov” # Rachel’s Cat`

(Using an Octothorpe, the `#` symbol either on its own line or at the end of a line makes everything else on that line a comment, which won’t be sent to the browser after it’s processed into javascript. It’s just there for humans. And also cats and bats.)

And you can use concatenation or interpolation to create strings that contain the value of variables.

`console.log “#{personTalkingTooMuch} is talking too much, but #{bestListener} rolls with it.”`
`console.log “Because “ + personTalkingTooMuch + " puts " + bestListener + ”’s food out each day.”`

## Arrays
An array is a list of values; the order matters because that’s how you’ll pull things out of the array. Elements of an array can be a variable or primitive type, or even an object, which we’ll learn about later.

`peopleExcitedForCoffeescript = [“Rachel”, bestListener, [“Emily”, “Jesse”, “Sally”], 43 ]`

And you can get values from an array if you know the index, which place it is in the array, starting at 0!
`peopleExcitedForCoffeescript[3]`

The .. syntax specifies a range.
`peopleActuallyExcited = peopleExcitedForCoffeescript[0..3]`

Other methods that you might expect as things you need to work quickly with Arrays are here, too:
`peopleExcitedForCoffeescript.length`

## Objects

Objects, called Hashes in other languages, are lists of keys and values. Think of the key as the name of an attribute, and the value as the specific value of that attribute.
```coffee
liskovCat = {
  eyeColor: "sometimes yellow, sometimes orange",
  furColor: "Black, Tan and White",
  ageInMonths: 7,
  favoriteFlyingMammal: "Bats"
}
```
(For readability, I added line breaks between the commas, but you don't need to.)

And after creating an object, read those attributes with a bracket syntax:
`console.log LiskovCat["eyeColor"]`
(Make sure to wrap the key in quotes!)

And you can set new attributes almost the same way:
```coffee
LiskovCat["favoriteBird"] = "Hummingbirds"
console.log LiskovCat
```

## Exercise
Given what we know so far,
- Create an Object representing you, including an `coffeescriptExcitementLevel` attribute, which should be a number.
- Read that attribute, and assign it to a variable, perhaps called `enthusiasm`
- Calculate a second variable, called `expectedFutureEnthusiasm` that is your current `enthusiasm`, multiplied by some number.
- Alert or log that value to the console with some descriptive text.
- :neckbeard:
- If you have time, create an array of hair colors, and assign a HairColor attribute to your object by selecting an element from that array.
