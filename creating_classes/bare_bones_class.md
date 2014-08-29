Coffeescript is most different from Javascript in the way it aims for object-oriented style inheritance. This aggravates some people, but $%*& the haters.
We'll use the keyword `class` and we'll always create a function call `contructor`.

## Create a class
```
class Mammal
```
Use a class to encapsulate specific behavior. In our case, we create a class that defines behavior specific to mammals.
Indent everything that's part of the class; the whitespace is how the Coffeescript compiler knows code is still part of this class.

Next, we'll create a specific function that's always named `constructor`, and is always run when a class is created. It's usually used to initialize values
```
class Mammal
  constructor: (@legCount, @finCount, @wingCount) ->
```

And we can add general mammalian behavior here.
```
class Mammal
  constructor: (@legCount, @finCount, @wingCount) ->

  canStayWarm: ->
    true
```

We can instantiate this class by calling:

```
cat = new Mammal(4, 0, 0)
```

## Inherit from a class
We'll use the keywords `extend` and `super` to make sure a class we create to inherit from mammal gets all the mammalian behavior.

The word `super` calls the constructor function of the class that you've extended from, mammal, with the values of legs, fins and wings.
```
class Cat extends Mammal
  constructor: ->
    super(4, 0, 0)
```

And we can add cat-specific behavior here, too.
```
class Cat extends Mammal
  constructor: ->
    super(4, 0, 0)

  noisyCat: ->
    console.log "MEOW MEOW MEOW MEOW MEOW"
    console.log "MEOW MEOW MEOW MEOW MEOW"
    console.log "MEOW MEOW MEOW MEOW. <3"
```
