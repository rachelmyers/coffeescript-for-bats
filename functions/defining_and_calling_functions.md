The challenge at the end of Control Flow would be easier and more readable if we defined functions that we could call each time we iterate.

The `=` is used to associate the name of a function with its definition, arguments to pass into the function immediately follow the `=`, and the definition is indented after an arrow, either `->` or =>`. (We'll get to the difference between them later; right now just stick with `->`.)
```
double = (orignalNumber) ->
  calculatedNumber = originalNumber * 2
```
And then we can call the function!
```
double(4)
double(6)
double(525600)
```
A more involved, but familiar example:
```
liskov =
  name:     "Liskov"
  age:      .6
  eyeColor: "sometimes yellow, sometimes orange",
  furColor: "Black, Tan and White",

logAttributes = (cat) ->
  for key, value of cat
    console.log "This cat's #{key} is #{value}!"

logAttributes(liskov)
```

This becomes much more useful if we have multiple cats, even an array of cats!

```
liskov =
  name:     "Liskov"
  age:      .6
  eyeColor: "sometimes yellow, sometimes orange",
  furColor: "Black, Tan and White",
max =
  name:     "Max"
  age:      .5
  eyeColor: "Black like his soul!",
  furColor: "Black",

cats = [liskov, max]

logAttributes = (cat) ->
  for key, value of cat
    console.log "This cat's #{key} is #{value}!"

for cat in cats
  logAttributes(cat)
```
And you can create functions that don't require arguments:
```
noisyCat = () ->
  console.log "MEOW MEOW MEOW MEOW MEOW"
  console.log "MEOW MEOW MEOW MEOW MEOW"
  console.log "MEOW MEOW MEOW MEOW. <3"

noisyCat()
```

## Returning
Sometimes you'll want to specify a return value, and not continue through an entire function. Use the keyword `return`.

```
catHoroscope = (name) ->
  return "You're a sleeping cat" if name.length > 12
  return "You're a running cat" if name.match('r') # If there's an `r` in the name
  return "You're a playing cat"

names = ["snuffleupagus", "liskov", "remy"]
for name in names
  console.log "Cat Horoscope says about #{name}: #{catHoroscope(name)}."
```
