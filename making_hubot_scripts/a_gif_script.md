## Starting simple

There are lots of simple Hubot scripts, ones that return a gif or witty text. We'll start there. (My personal fave is [`mean girls me`](https://github.com/github/hubot-classic/blob/master/scripts/meangirls.coffee).)

To start, follow the [Hubot Development Instructions](https://github.com/github/hubot-classic#development):
```shell
$ boxen hubot-classic
$ cd ~/github/hubot-classic
$ script/server [--debug]
```

Since this is a real repo, and not in a sandbox, we need to create a branch before we start playing around.
`$ git checkout -b awesome-new-gif-script`

To start, we can create (in a new file) a new response for Hubot, by defining
```
  robot.respond /beyonce me/i ->
    beyonceSaying = "If I’m not sleeping, nobody’s sleeping."
```
And because, we need it to hook in to existing Hubot code, we need to wrap that in
```
module.exports = (robot) ->
  robot.respond /beyonce me/i ->
    beyonceSaying = "If I’m not sleeping, nobody’s sleeping."
```
But this is kind of boring. It's way better if we get together a collection of things, and create an array:
```
beyonceQuotes = [
"If I’m not sleeping, nobody’s sleeping.",
"You’re never too smart to lose. It happens.",
"I feel like I’m an adult. I’m grown. I can do what I want. I can say what I want. I can retire if I want."
]
```
...
