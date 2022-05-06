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

# Credits
Some of the code is taken from [Ash](https://github.com/arc-spwn/ash), for parsing command line arguments.

(hey FL1P the name is still from ChromeOS)

Potato

mostacho

cheese

:skull:
