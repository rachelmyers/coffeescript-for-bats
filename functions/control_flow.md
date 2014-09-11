Sometimes you want to only take an action under certain conditions, or you want to repeat actions in a loop until a condition is met.
Programmers call that "control flow", controlling the code paths you'll take.

## Comparisons
Comparisons that in other languages use the sumbols `=` or `!=`, use words like `is` or `isnt`.

Try checking the output of these expressions:
- `console.log 7 is 7`
- `console.log 7 is 3 + 4`
- `console.log 7 isnt 12`
- `console.log 7 > 3`



The words `and` and `or` are coffeescript keywords that correspond to the symbolic logic meaning of `⋀` and `⋁`. (If you're more familiar with Ruby, it's `&&` and `||` there.)
Try making expressions using `is`, `isnt`, `and` and `or`, like
`7 > 5 or 4 < 3`

## Conditionals
The keywords used to create conditionals are `if`, `else`, and `else if`.

And this is the first point we'll run into the importance of whitespace in Coffeescript. We won't need an `end` in our conditional, because the indentation will tell the compiler where it ends.

```
catAge = 5

if catAge < 1
  console.log "That cat is still a kitten!"
else if catAge < 10
  console.log "That cat is a normal cat."
else
  console.log "Wow. That cat is old!"
```

## Looping through a collection
`for` and `in` are also keywords that we can use to loop through an array or objects.
The indentation in block of the loop is important; when the indentation outdents, it means the the block has ended.

```
catAges = [8, .2, 3, 5, .6, 13, 4]

for catAge in catAges
  if catAge < 1
    console.log "That cat is still a kitten!"
  else if catAge < 10
    console.log "That cat is a normal cat."
  else
    console.log "Wow. That cat is old!"
```

And we can do something similar with Objects:
```
liskov =
  name:     "Liskov"
  age:      .6
  eyeColor: "sometimes yellow, sometimes orange"
  furColor: "Black, Tan and White"

for key, value of liskov
  console.log "Liskov's #{key} is #{value}!"
```

## Challenge

- Create an Array of cats, and iterate through the array, logging something as you do.
- Then create an Array of Objects about different cats.
- As you iterate through the Array of Objects, also iterate through the attributes of the object.
