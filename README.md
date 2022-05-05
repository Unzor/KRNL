# KRNL
A library that lets you create operating systems/shells in SPWN.

# How to install?
Run "spghtt" ([install it first](https://github.com/Unzor/spghtt)), use the "install" action, and type in "krnl".
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
