---
layout: page
title: "Wiki"
---

This wiki page is a collection of bits and pieces of info.  

For further information click [CoderDojoBalwyn @ Balwyn Library](https://zen.coderdojo.com/dojos/au/balwyn-vic/balwyn-balwyn-library) or [CoderDojoBalwyn Website](https://balwynau.wixsite.com/coderdojo)  


### (a) Hello World App

Hello World App by Rockycape - You can simply select and then copy the code below and past into a new blank app on bitsbox.com  

```markdown
chaseme = text('<>',100,100)
catchme = text('Hello World - You can\'t catch me!',100,500)
               function drag() {
  chaseme.move(x,y,100)
  if (chaseme.hits(catchme)) {
    catchme.move(random(1,400),random(1000))
  }
}
```

### (b) javascript apps  

[Snake App](https://rockycape.github.io/snake.html)  

[Pacman App](http://www.flashmonkey.co.uk/lab/pacman/)  

[Pacman App Info](http://www.flashmonkey.co.uk/css-javascript-pacman/) 

### (c) favourite web apps

[QRDROID QR generater](http://qrdroid.com/generate/) 

[Google Doodle Pacman App](https://www.google.com/doodles/30th-anniversary-of-pac-man)




### (d) github pages
[customising css and html in your jekyll theme on github pages](https://help.github.com/articles/customizing-css-and-html-in-your-jekyll-theme/)  

[how to add a favicon to github pages](https://medium.com/@LazaroIbanez/how-to-add-a-favicon-to-github-pages-403935604460)  



### (e) For more details see 

For more details see [Writing on GitHub / Basic writing and formatting syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax/) or  [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/)  

### (f) Jupyter Notebook (interactive python) 

Jupyter Notebook is an interactive version of python that conveniently runs in your internet browser.  
You can install Jupyter Notebook after intalling the python language locally on you computer OR you can install Jupyter Notebook on the web with both [github.com](github.com) and [mybinder.org](https://mybinder.org/)  

Once you've got Jupyter Notebook up and running here are some resources you might find useful to learn more:  

[awesome jupyter](https://github.com/markusschanta/awesome-jupyter#awesome-jupyter-)  

### (g) Keyboard and other commands for Jupyter Notebook  

To execute code:  

**`shift` + `enter`**  

**N.B.** when working with Mardown in Jupyter Notebook, you will need to:  

(a) select the cell  
(b) type the **`m`** key to turn the cell into Markdown  
(c) type **`shift` + `enter`** to show the contents of the cell as Markdown  

*Remember that there are two modes:  
command mode & edit mode*  

In command mode:  

move up and down cells with the **`⇧`** and **`⇩`** keys  
**`m`** turns a cell into Markdown  
**`y`** turns a cell into code  
**`z`** undo cell operation  
**`shift`+`x`** redo cell operation  
**`c`** copy cells  
**`v`** paste cells below  

### (h) Jupyter Turtle

```
from mobilechelonian import Turtle
t=Turtle()
colour = [ "red","purple","blue","green","orange","yellow"]
t.home()
t.pendown()
for c in range(360):
    t.pencolor(colour[c % 6])
    t.forward(c)
    t.left(59)
```

![jupyter turtle drawing](assets/jupyterturtledrawing.jpg) <!-- This works for jpeg in assets folder below root -->


```
#sierpinski triangle #1
from mobilechelonian import Turtle
t=Turtle()
t.right(30)
t.speed(10)
def sierpinski(size, order):
    if order == 0:
        return
    else:
        for i in range(0,3):
            t.forward(size)
            sierpinski(size/2,order-1)
            t.backward(size)
            t.left(120)
            
sierpinski(100,5)
```

![sierpinskitriangle01](assets/sierpinskitriangle01.png)


```
#sierpinski triangle #2
from mobilechelonian import Turtle
t=Turtle()
#move turtle to bottom right corner
t.penup()
t.speed(10)
t.backward(200)
t.right(90)
t.forward(200)
t.left(90)
t.pendown()

angles = [0, 120, 240]
colors = ["red","blue","purple"]


def draw_equi_triang(size):
    for i in range(3):
        t.forward(size)
        t.left(120)

def shift_turtle(size, angle):
    t.left(angle)
    t.penup()
    t.forward(size)
    t.pendown()
    t.right(angle)

def sierpinski(order, size, colorChangeDepth = -1):
    if order == 0:
        draw_equi_triang(size)
    else:
        if colorChangeDepth == 0:
            for (ind, angle) in enumerate (angles):
                t.pencolor(colors[ind])
                sierpinski(order-1, size/2, colorChangeDepth-1)
                shift_turtle(size/2, angle)
        else:
            for angle in angles:
                sierpinski(order-1, size/2, colorChangeDepth-1)
                shift_turtle(size/2, angle)

sierpinski(4,300)
```

![sierpinskitriangle02](assets/sierpinskitriangle02.png)

```
#sierpinski triangle #3
from mobilechelonian import Turtle
t=Turtle()
#move turtle to bottom right corner
t.penup()
t.speed(10)
t.backward(200)
t.right(90)
t.forward(200)
t.left(90)
t.pendown()

angles = [0, 120, 240]
colors = ["red","blue","purple"]


def draw_equi_triang(size):
    for i in range(3):
        t.forward(size)
        t.left(120)

def shift_turtle(size, angle):
    t.left(angle)
    t.penup()
    t.forward(size)
    t.pendown()
    t.right(angle)

def sierpinski(order, size, colorChangeDepth):
    if order == 0:
        draw_equi_triang(size)
    else:
        if colorChangeDepth == 0:
            for (ind, angle) in enumerate (angles):
                t.pencolor(colors[ind])
                sierpinski(order-1, size/2, colorChangeDepth-1)
                shift_turtle(size/2, angle)
        else:
            for angle in angles:
                sierpinski(order-1, size/2, colorChangeDepth-1)
                shift_turtle(size/2, angle)

sierpinski(4,300,0)
```
![sierpinskitriangle03](assets/sierpinskitriangle03.png)

### (i) Markdown

Best Practice for writing with Markdown  
(1) Don't put tabs or spaces in front of your paragraphs and keep lines left-aligned  
(2) End a line with two or more spaces '  ', and then type return  

### (j) Markdown resources

[Markdown summary sheet](https://www.markdownguide.org/cheat-sheet/)  
[Paste to Markdown](https://euangoddard.github.io/clipboard2markdown/)

### (k) Sublime Text

You may want to edit your Markdown with a text editor like Sublime Text.  To make it easier to visualise the formatting of ending a line with two or more spaces we have installed both **Package Control** and then **MarkdownEditing** to Sublime Text:  

### Package Control
---------------

It is highly recommended to install MarkdownEditing with [Package Control](https://packagecontrol.io/) as it automatically installs required dependencies and keeps all packages up to date.

1.  [Install Package Control](https://packagecontrol.io/installation) if you haven't yet.
2.  Open Command Palette (`Ctrl` + `Shift` + `P` (Windows, Linux) or `⌘` + `⇧` + `P` on Mac)
3.  Type *Install Package* and hit `Enter` to display a list of available packages.
4.  Type *MarkdownEditing* and hit `Enter` to install the package.

### (i) Jekyll

Remember once you've installed Jekyll locally on your Mac
1. Open terminal and navigate to the root folder for your static site
2. start Jekyll with:
```
jekyll serve
```

### (j) [youtube-dl](http://ytdl-org.github.io/youtube-dl/download.html)

steps to get up and running with youtube-dl for a vanilla Mac install as follows:

1. install brew ((Home)brew on its own acts like a command-line App Store. It's safe if you know what you're downloading)
2. brew install youtube-dl (youtube-dl is a solution to download streamed audio and video)
3. brew install ffmpeg (FFmpeg is a solution to record, convert and stream audio and video)

NB youtube-dl is able to download streamed video from ABC iview via the terminal:

```
youtube-dl https://iview.abc.net.au/blah/blah/blah
```


<!--
☯️

### (f) markdown

Syntax highlighted code block example
```markdown
blah blah blah
```

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)

-->
