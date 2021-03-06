# A
[![Go Report Card](https://goreportcard.com/badge/github.com/as/a)](https://goreportcard.com/badge/github.com/as/a)
[![CircleCI](https://circleci.com/gh/as/a/tree/master.svg?style=svg)](https://circleci.com/gh/as/a/tree/master)

A is a text editor. It is inspired by the Sam and Acme text editors for the Plan 9 operating system.

![paint](a.png)

- Written in Go (no dependencies)
- Native Multi-Platform Graphics (as/frame)
- Closely resembles the Acme and Sam text editors.
- Optimized for editing huge binary files. 
  - The underlying frame implementation (see as/frame) does not eschew null bytes.
  - Experimental UTF-8 support 
- Standard UNIX keyboard shortcuts `No vi/emacs tricks`
- Mouse chording
- Command Language
  `Edit command language is 80% implemented (slow)`
- Structure highlighting

![paint](install.png)
![paint](b.png)


This repository will change frequently, things will improve unexpectedly. See issues.

# install
Because the other packages in my namepace are frequently updated , I recommended using go get -u

`go get -u -t github.com/as/a`
 
# usage
a [file ...]

# differences and issues
- Compare to the true Acme
https://github.com/as/a/wiki/Alterations

- issues
https://github.com/as/a/issues

# hints
To reshape the windows and columns, click on the invisible 10x10px sizer that I haven't rendered yet with the middle mouse button. Hold the button down and move the window to the location. Release the button.

# edit
- 80% of the sam command language is implemented.

Edit ,x,the standard editor is any editor,x,any editor,c,ed,

# commands
- Currently only in CWD
- Put ```[go build]``` in the tag
- Double click inside ```[```
- Middle click to execute

# look
- Right click on a string
- If its a file, it will open it
- If win32, it will also move the mouse

# mouse
```
1 Select text/sweep
1-2 Snarf (cut)
1-3 Paste
2 Execute select
3 Look select
```

# keyboard
```
^U  Delete from cursor to start of line.
^W  Delete word before the cursor.
^H  Delete character before the cursor.
^A  Move cursor to start of the line.
^E  Move cursor to end of the line.
^+  Increase font size
^-  Decrease font size
```

# extras
- Looking (right click) in the main tag finds the result in all open windows
![paint](jump.png)    

# purpose
- ACME SAC doesn't run on my computer
- The solution is to create a text editor from scratch then

# future
- Fixing the bugs
- Cleaning the code up
- Live multi-client editing
- Go specific ast/compiler stuff
- Better CMD exec
- File system interface to shiny events

# see also
History of good text editors

- `The Acme User Interface for Programmers` (Rob Pike)
- `A Tutorial for the Sam Command Language` (Rob Pike)
- Plan 9 
- Inferno
- Acme SAC
