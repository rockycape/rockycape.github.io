---
layout: page
title: "Wiki"
---

This wiki page is a collection of bits and pieces of info relating to computer science for kids 7 - 70! 



|a|b|c|
|--- | --- | ---|
|`code block`|`code block`|`code block`|
|`code block`|`code block`|`code block`|

### (a) Bitsbox.com Apps

Hello World App - You can simply select and then copy the code below and past into a new blank app on bitsbox.com  

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


Monster Invaders App - You can simply select and then copy the code below and past into a new blank app on bitsbox.com  

```markdown
fill('pixel sky')
counter = 1
step = 30
points = 0
speed = 16
hero = stamp('pixel knight', 386, 880)
score = text(points, 345, 50, 'white')
message = text('Ready?', 300, 500, 50, 'white')


function tap() {
  sound('laser')
  shot = stamp('pixel sword', hero.x-50, hero.y)
  shot.move(NORTH, 1500, 2000)
  hero.move(x + 50, hero.y, 500)
}


function animate() {}


function column(i) {
  x = i * 110
  stamp('cyclops', x, 100)
  stamp('cyclops', x, 180)
  stamp('cyclops', x, 260)
  stamp('cyclops', x, 340)
}


function spawn() {
  message.change('')
  repeat(column, 5)
  loop = animate
}
delay(spawn, 2000)


function logic() {}


function march(alien) {
  alien.move(alien.x + step, alien.y)
}


function check(sword) {
  strikes = sword.hits('cyclops')
  if (strikes.length > 0) {
    sound('hit')
    strikes[0].explode()
    sword.hide()
    points = points + 100
    score.change(points)
  }
}


function animate() {
  find('pixel sword').forEach(check)
  counter = counter + 1
  if (counter>= speed) {
    counter = 1
    sound('putt putt')
    aliens = find('cyclops')
    aliens.forEach(march)
    logic()
  }
}


function drop(alien) {
  alien.move(DOWN)
}


function logic() {
  if (offscreen(aliens)) {
    step = -step
    aliens.forEach(drop)
    aliens.forEach(march)
  }
 if (aliens.length == 0) {
   loop = null
   message.change('Next wave.')
   speed = speed-2
   delay(spawn, 2000)
 }
  if (hero.hits('cyclops')) {
    hero.explode()
    message.change('Game over')
  }
}

```




### (b) javascript apps  

[How to learn javascript properly](http://javascriptissexy.com/how-to-learn-javascript-properly/)

[Snake App](https://rockycape.github.io/snake.html)  

[Pacman App](http://www.flashmonkey.co.uk/lab/pacman/)  

[Pacman App Info](http://www.flashmonkey.co.uk/css-javascript-pacman/) 

### (c) favourite web apps

[QRDROID QR generater](http://qrdroid.com/generate/) 

[Google Doodle Pacman App](https://www.google.com/doodles/30th-anniversary-of-pac-man)




### (d) github.com & vscode.dev

Microsoft have a couple of good webapps that may help you with your coding.  

The first webapp is called [github.com](github.com) 
Create yourself a free github account and take a look further down this page for some of things you can do with it including creating your own website.

The second webapp is called [vscode.dev](vscode.dev)

You may want to write or edit your code or Markdown with vscode.dev which is Microsoft's code editor. Conveniently you can start using vscode.dev by signing in with your github username and password.

### (e) github pages  

[customising css and html in your jekyll theme on github pages](https://help.github.com/articles/customizing-css-and-html-in-your-jekyll-theme/)  

[how to add a favicon to github pages](https://medium.com/@LazaroIbanez/how-to-add-a-favicon-to-github-pages-403935604460) 

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



### (l) Create a great looking website using Jekyll minima theme and host for free on Github Pages

Remember you are not installing anything locally on your PC/Mac but are installing on Github on the internet so the first requirement is to already have or create a github account.

1. sign in to your github account at [github.com](github.com) 
2. go to ---> [https://github.com/new/import](https://github.com/new/import) 
3. import the following existing repository ---> [https://github.com/jekyll/minima](https://github.com/jekyll/minima)
4. configure your new website and then add content 


### (m) Embed youtube videos on your Jeckyll minima website hosted for free on Github Pages

[https://github.com/nathancy/jekyll-embed-video](https://github.com/nathancy/jekyll-embed-video)

### (n) Selecting Text in Columns in a PDF on a Mac

A solution to a constant source of frustration for me: I have a PDF --- [like this one](http://www.islandarchives.ca/fedora/repository/vre:islemag-batch2-235/OBJ/04_St_Eleanors_the_veneered_village_p_3-8.pdf) --- that has text formatted in multiple columns:

![PDF with text in columns](https://ruk.ca/sites/ruk.ca/files/media.ruk.ca/multipdf.jpg)

I want to copy some text from the PDF, but when I do this by simply clicking and dragging the mouse, *all* of the columns of text get selected:

![PDF with text in columns, text selected across columns](https://ruk.ca/sites/ruk.ca/files/media.ruk.ca/multipdf2.jpg)

The secret: **use Option + Drag** to select the text. Hold down the Option key, in other words, while you drag a box around the text you want to select:

![PDF with text in columns, text selected from one column](https://ruk.ca/sites/ruk.ca/files/media.ruk.ca/multipdf3.jpg)

The result is *just the text I want, from the single column I want it from*:

> But St. Eleanors was not first settled by the English. In the last quarter of the 18th century, the southern shore of Malpeque Bay was populated by no fewer than 23 Acadian families, several of them refugees from the English expulsion of Acadians in Nova Scotia 20 years earlier. They bore familiar French names like Arsenault, Gallant, Poirier, and Bernard, and they had their own church, a little chapel situated on the east side of Rayner's Creek. Most of the settlement was in Lot 17, which had been acquired in 1767 by two brothers, B. and P. Burke.


### (o) AirMessage - Cannot Connect an Account During Server Setup

Cannot Connect an Account During Server Setup
=============================================

Hi there,

I had AirMessage running before upgrading to 4.x, and now upon setting up my server again I click "Connect an Account", then the below popup to allow AirMessage to use localhost, then it opens Chrome and nothing happens.

I've been trying to figure out if I had made a home network change or something, but this happens when I'm on my phone's hotspot as well. And I couldn't find any resolution in the help docs.

Any one else having this problem?

-----

[jtking51](https://www.reddit.com/user/jtking51/)

Update: So I read a post further down talking about this same issue and they said they had to let Airmessage open chrome, meaning it couldn't be open already. I installed chrome, opened it, then closed it changed it to my default browser. Opened Airmessage and clicked the Connect an account option. It opened Chrome and I had the option to login to my google account finally. Give that a try.

-----

Update: After reading the above I set Safari as my default browser and then opened Airmessage server (on my Mac) and clicked the Connect an account option. It opened Safari and I had the option to login to my google account finally.


### (p) importing AVCHD video files from Sony Alpha NEX-F3 camera SD card to apple mac and converting to MP4 via Handbrake

a. Put the SD card into the apple mac
b. Navigate to PRIVATE folder and select AVCHD file
c. right click AVCHD file and choose *show package contents*
d. select BDMV file and choose *show package contents*
e. click to open *STREAM folder* to reveal .MTS files
f. select a .MTS and open in Handbrake to convert to MP4



<!--  

### (j) [youtube-dl](http://ytdl-org.github.io/youtube-dl/download.html)

steps to get up and running with youtube-dl for a vanilla Mac install as follows:

1. install brew ((Home)brew on its own acts like a command-line App Store. It's safe if you know what you're downloading)
2. brew install youtube-dl (youtube-dl is a solution to download streamed audio and video)
3. brew install ffmpeg (FFmpeg is a solution to record, convert and stream audio and video)

NB youtube-dl is able to download streamed video from ABC iview via the terminal:

```
youtube-dl https://iview.abc.net.au/blah/blah/blah
```


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
