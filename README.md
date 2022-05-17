# KRNL
A library that lets you create operating systems/shells in SPWN.

# How to install?
Run "spghtt" ([install it first](https://github.com/Unzor/spghtt)), use the "install" action, and type in "krnl". 

You can also just copy the code from the repo, paste it in a file, and use `import "krnl.spwn"` instead.

Now create a new file in the same directory named "index.spwn", and paste this in:
```js
let krnl = import krnl
krnl.createCommands({
	hworld: (args) {
	    let args = krnl.parse(args)
		if (args.args.length != 0) {
			if (args.args[0] == "--test" || args.args[0] == "-t") {
				$.print("Hello world, with test!")
			}
		} else {
		    $.print("Hello World!")
		}
	}
})

krnl.init("Welcome to some operating system I made. Run 'hworld' to echo a Hello World example, and add -t or --test to test out arguments.")
```
Now run "spwn build index.spwn -l", and you should see a command line prompt. Type in "hworld", and you will see a "Hello World" message!

Now try adding -t or --test to the command. You should see "Hello world with test!" in the prompt. If you see this, it worked!

# Credits
Some of the code is taken from [Ash](https://github.com/arc-spwn/ash), for parsing command line arguments. Thanks to Specky, Fl1p, SeanDaSheep, and zTags for writing the code.

Potato

mostacho

cheese

i like minorities :skull:
