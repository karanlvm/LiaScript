<!--
author:   Karan Vasudevamurthy

email:    karanlvm123@gmail.com

version:  0.0.1

language: en

narrator: US English Female
script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
          https://felixhao28.github.io/JSCPP/dist/JSCPP.es5.min.js

import: https://raw.githubusercontent.com/LiaTemplates/algebrite/0.2.1/README.md 
        https://raw.githubusercontent.com/liaTemplates/TextAnalysis/main/README.md

-->

# Introduction to LiaScript

LiaScript is an open-source programming language designed for creating interactive online courses and tutorials. It allows authors to write instructional material in a simple text format, which can be easily converted into a variety of web-based formats, including HTML, Markdown, and LaTeX.

One of the key features of LiaScript is its ability to embed interactive elements directly into the course material. For example, authors can include quizzes, coding exercises, and interactive visualizations, which learners can interact with directly on the page. This helps to make the learning experience more engaging and effective.

LiaScript also includes support for a range of programming languages, including JavaScript, Python, and R, allowing authors to include code examples and demonstrations in their courses.

Overall, LiaScript is a powerful tool for creating engaging and interactive online courses and tutorials, and is well-suited for use in educational settings.


# LiaScript Setup

1) [Download VS Code](https://code.visualstudio.com/download)

2) Navigate to the extentions tab in VS code

3) Download [LiaScript-Preview](https://marketplace.visualstudio.com/items?itemName=LiaScript.liascript-preview)

4) Create a new README.md file and press alt+L to open up the live server preview for the course




## Writing your course

You can use common [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) syntax to create your course.




### Adding lists

1. Ordered lists can be create by simply specifiying a number followed by a (.) before the title of the list.
2. Unordered lists can be created by using the (*) symbol before the title of the list. 

For Example: 

* Unordered List 1
* Unordered List 2

You can also create tables like this- 

| Header 1 | Header 2 |
| :------- | :------- |
| Item 1   | Item 2   |

Hint: create the table using [ | ] and the partions between the rows with [ :----- ] symbols 

Tables are elaborated below. 

### Adding Images

![Greek vase painting: seated young man writes on a wax tablet with a stylus](https://www.cvaonline.org/images/pottery/painters/keypieces/tiverios/21-p156bottom-medium.jpg "The so-called 'School cup' signed by the vase painter Douris. The seated man writes on a wax tablet with a stylus, showing the boy to the right how to do it. Early 5th c BCE. Berlin, Staatliche Museen.")

Images can be added using '! [Alt Text] ( image link)'  {No spaces}

### Adding music

?[Sappho: Ode to Aphrodite](http://homoecumenicus.com/ioannidis_sappho_aphrodite.mp3 "Ancient Greek lyrical poem by Sappho (610-580BC). Original music by IOANNIDIS")

Audios can be added using '? [ Alt Text] ( Audio Link)' 

### Adding Videos

!?[Greek Art History from Goodbye-Art Academy](https://www.youtube.com/watch?v=Me0Psn6VrTg "_Black-Figure Dinos (Mixing Vessel); Warships (int.); Heroic Scenes (top)_, c. 520-515 BC. Circle of Antimenes Painter (Greek, Attic, active c. 530-510 BC). Veramic; diam. 50.8 cm; overall: 33.6 cm; rim diam. 34 cm. The Cleveland Museum of Art, Jon L. Severance Fund, 1971.46")

Since a video is nothing but images and audio, the syntax is quite similar and it is ' !? [ Alt Text] (Link)' 

### Other Links 

??[Neck Amphora](https://sketchfab.com/3d-models/197016-neck-amphora-0bb2525bdd734bf69d5a7b2b051928ad "_Neck Amphora_ (515-510 BC). Painter of Berlin 1899 (Greek). Greece, Attic, 6th Century BC Black-figure terracotta. Diameter: 29 cm (11 7/16 in.); Overall: 39.8 cm (15 11/16 in.). Andrew R. and Martha Holden Jennings Fund 1970.16 ") 

??[Capacitor simulation by Falstad](https://www.falstad.com/circuit/circuitjs.html?startCircuit=cap.txt "A capacitor is a device that stores charge. As current flows into the capacitor, the voltage across the capacitor increases. As its voltage approaches the source voltage (the 5V voltage source shown on the left), the current flowing into the capacitor decreases.") 


Links that do not fall under the conventional three categories of audio, videos and images can be linked using the '??' prefix.

## Animations 
Animations in LiaScript are associated with double braces `{begin-end}`. 

    --{{1}}--
Add an number in double braces to the head of a block let it appear at a
certain step.

      {{1}}
> Animations in LiaScript are associated with double braces `{begin-end}`.

     {{2-3}}
| I  will              | begin at               |
| -------------------- | ---------------------- |
| animation-step **2** | and end at step **3**. |


    --{{2}}--
You can add a number in double braces and the text below it, will be TTS. 

## Tables and charts

### 1. Basics

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Tables are created by using `|` symbols to define the columns. Below the heading of each column, `-------` is added if a `:` is added on the right side of the hypens, then the text becomes right justified. Add it on both the ends and the text becomes center justified. By default, all text is left justified.  

### 2. Bar charts 

| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |             02 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |

As the amount of similar data increases, LiaScript will create charts to visualize the data. 

### 3. Smart Visualization

| Music-Style 1994 | Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
|:---------------- | -------:| -------:| ------:| -------:| ---------:| -----:|
| Student rating   |      50 |      50 |    100 |     200 |       350 |   250 |


The chart created doesn't always have to be a bar chart. LiaScipt will automatically try to find an appropriate visualization based on the data.


### 4. Combination with animations

<!-- data-transpose data-type="funnel" -->
| Music-Style {0-1}{1994} {1}{2014} |      Student rating |
|:--------------------------------- | -------------------:|
| Classic                           |   {0-1}{50} {1}{20} |
| Country                           |   {0-1}{50} {1}{30} |
| Reggae                            |                 100 |
| Hip-Hop                           | {0-1}{200} {1}{220} |
| Hard-Rock                         | {0-1}{350} {1}{400} |
| Samba                             | {0-1}{250} {1}{230} |

You can combine animations into tables as well. If you would like to specify a type of chart that should be used for visualization,  `<!-- data-transpose data-type="type-of-chart" -->` is the syntax. 

### 5. Customization

<!--
data-type="heatmap"
data-title="Seattle mean temperature in Fahrenheit"
data-ylabel="hours"
data-xlabel="month"
data-show
data-transpose
-->
| Seattle |  Jan |  Feb |  Mar |  Apr |  May |  Jun |  Jul |   Aug |  Sep |  Oct |  Nov |  Dec |
| -------:| ----:| ----:| ----:| ----:| ----:| ----:| ----:| -----:| ----:| ----:| ----:| ----:|
|       0 | 40.7 | 41.5 | 43.6 | 46.6 | 51.4 | 56.0 | 60.5 |  61.2 | 57.0 | 50.1 | 44.1 | 39.6 |
|       2 | 40.2 | 40.7 | 42.7 | 45.3 | 50.0 | 54.4 | 58.5 |  59.2 | 55.4 | 49.2 | 43.5 | 39.3 |
|       4 | 39.7 | 40.0 | 41.9 | 44.4 | 48.9 | 53.2 | 57.0 |  57.7 | 54.2 | 48.6 | 43.1 | 38.9 |
|       6 | 39.6 | 39.5 | 41.3 | 44.2 | 49.5 | 54.2 | 57.8 |  57.4 | 53.6 | 48.2 | 42.8 | 38.7 |
|       8 | 39.6 | 39.9 | 42.9 | 47.1 | 52.7 | 57.3 | 61.3 |  61.1 | 56.7 | 49.5 | 43.1 | 38.7 |
|      10 | 41.3 | 42.7 | 46.4 | 50.7 | 56.4 | 60.9 | 65.2 |  65.4 | 60.9 | 52.8 | 45.5 | 40.4 |
|      12 | 43.8 | 46.0 | 49.5 | 53.8 | 59.6 | 64.3 | 69.4 |  69.8 | 65.1 | 56.0 | 47.8 | 42.6 |
|      14 | 45.1 | 47.7 | 51.3 | 55.9 | 61.9 | 66.9 | 72.6 |  73.2 | 67.7 | 57.8 | 48.8 | 43.6 |
|      16 | 44.5 | 47.5 | 51.4 | 55.9 | 62.3 | 67.5 | 73.9 |  74.3 | 68.2 | 57.4 | 47.8 | 42.6 |
|      18 | 42.6 | 44.7 | 48.7 | 53.8 | 60.3 | 65.9 | 72.3 |  72.2 | 64.6 | 53.9 | 46.0 | 41.2 |
|      20 | 42.0 | 43.3 | 46.4 | 50.2 | 56.0 | 61.4 | 66.9 |  66.6 | 60.7 | 52.3 | 45.2 | 40.7 |
|      22 | 41.4 | 42.5 | 45.0 | 48.3 | 53.5 | 58.2 | 63.2 |  63.5 | 58.7 | 51.1 | 44.5 | 40.1 |


Similarly, we can also create heatmaps using similar syntax and also add data-title, data-ylabel, data-xlabel etc..

## ASCII-Art


### Type 1

                                    Multiline
    1.9 |
        |                 *
      y |               *   *
      - | r r r r r r r*r r r*r r r r r r r
      a |             *       *
      x |            *         *
      i | B B B B B * B B B B B * B B B B B
      s |         *               *
        | *  * *                     * *  *
     -1 +------------------------------------
        0              x-axis               1



### Type 2


```` ascii
                                       Peer A
                                       Server-Reflexive    +---------+
                                       Transport Address   |         |
                                       192.0.2.150:32102   o         |
                                           |              /|         |
                         TURN              |             /^|  Peer A |
   Client's              Server            |            / ||         |
   Host Transport        Transport         |           /  ||         |
   Address               Address           |      ____/   |+---------+
  10.1.1.2:49721       192.0.2.15:3478     |+-+  /      Peer A
           |               |               ||N| /       Host Transport
           |   +-+         |               ||A|/        Address
           |   | |         |               v|T|     192.168.100.2:49582
           |   | |         |               /+-+
.---------.|   | |         |o---------o   /              #---------#
|         ||   |N|         ||         | _/               |         |
| TURN    |v   | |         v| TURN    |/                 |         |
| Client  |----|A|----------| Server  #------------------|  Peer B |
|         |    | |^         |         |^                ^|         |
|         |    |T||         |         ||                ||         |
'---------'    | ||         o---------o|                |#---------#
               | ||                    |                |
               | ||                    |                |
               +-+|                    |                |
                  |                    |                |
                  |                    |                |
            Client's                   |            Peer B
            Server-Reflexive    Relayed             Transport
            Transport Address   Transport Address   Address
            192.0.2.1:7000      192.0.2.15:50000    192.0.2.210:49191
````

### Combining ASCII with animations 

---

```` ascii
😎                   👩

Bob                Alice
 |   "{1}{hello}"    |
 +------------------>|
 |                   |
 | "{2}{How r you?}" |
 |<- - - - - - - - - |
 |                   |
Bob                Alice

 😎                  👩
````

---

## Checkboxes

- [x] Task 1
- [ ] Task 2

The syntax to define the checkboxes are `- [ ] Task 2` and adding a `x` between the [] will make the box marked. 

## Quizes

With LiaScript it is possible to create quizes (single answer and multiple answers). It is also possible to provide hints

### Single answer 

If $ I = \int (3x^{2}+125x+64) dx $, then what is $\int_{0}^{1} I dx$ equal to?

[( )] $\frac{159}{2}$
[( )] $\frac{171}{2}$
[( )] $\frac{221}{2}$
[(X)] $\frac{225}{2}$


Each option can be created using `[( )]` and the right answer can be marked by `[(X)]`

### Adding hints and solutions


Hints can be added using `[[?]]` and the answer can be defined by adding `*********************` before and after the solution



If $ I = \int (3x^{2}+125x+64) dx $, then what is $\int_{0}^{1} I dx$ equal to?

[( )] $\frac{159}{2}$
[( )] $\frac{171}{2}$
[( )] $\frac{221}{2}$
[(X)] $\frac{225}{2}$
[[?]] Integrate and apply the limits.
**************************************

__Consider__ $I = \int_{0}^{1} (3x^{2}+125x+64) dx$

Integrate

$$
I = \Bigg[ \frac{3x^2}{3} + \frac{125x^2}{2} + 64x \Bigg]_{0}^{1}
$$

==>

$$
   \Bigg( 3x^2 + \frac{125x^2}{2} + 64x \Bigg)_{0}^{1}
$$

==>

$$
   1 + \frac{125}{2} + 64
$$

==>

$$
   \therefore I = \frac{225}{2}
$$


**************************************


### Muliple answers 

Can you define a quiz with less effort?

- [[ ]] Empty means not checked
- [[X]] Uppercase `X` means checked ...
- [[x]] ... and lowercase `x` too ...
- [[ ]] **as defined in the first line** ...

### Enter your answer 

Syntax for the answer is : `[[answer]]`
What did the *fish* say when he hit a *concrete wall*?

    [[dam]]


## Coding

Teaching other language-basics is also possible, for this example we applied [JSCPP](https://github.com/felixhao28/JSCPP)
to run simple C++ programs:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 120;
    int rslt = 0;
    for(int i=1; i<a; ++i) {
        rslt += i;
        cout << "rslt: " << rslt << endl;
    }
    cout << "final result = " << rslt << endl;
    return 0;
}
```
<script>
  var output = "";
  JSCPP.run(`@input`, "", {stdio: {write: s => { output += s }}});
  output;
</script>


### More Coding 

                --{{0}}--
Multiple different code snippets can be combined to form a larger projects too.
It requires to write them in a row.
You can give them names, if you add a second parameter after the highlighting definition.
Add a `+` or `-` to the front of your filename, in order to indicate, if it should be visible by default or not.

                --{{1}}--
As previously mentioned the `@input` macro gets substituted by the input of the editor, but you can pass also a number to indicate which macro should be substituted by which code block (`@input(0)` is equivalent to `@input`).

```` markdown
``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.online) {
  who + " is online"; }
else {
  who + " is NOT online"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "online"     :  true
}
```
<script>
  // insert the JSON dataset into the local variable data
  let data = @input(1);

  // eval the script that uses this dataset, but just
  // inserting the @input, which already contains JS code
  // would be also fine ... 
  eval(`@input(0)`);
</script>
````

                               --{{2}}--
The result is a project which consists of two files.
Each file can be edited separately, while the script tag provides only some basic glue-code that tells LiaScript what to do with the input. 

                                 {{2}}
``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.online) {
  who + " is online"; }
else {
  who + " is NOT online"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "online"     :  true
}
```
<script>
  // insert the JSON dataset into the local variable data
  let data = @input(1);

  // eval the script that uses this dataset
  @input
</script>

## Math
``` text
(3 * x - 5x)^3 * (x + x)

60!
```
@Algebrite.eval


``` text
f=sin(t)^4-2*cos(t/2)^3*sin(t)

f=circexp(f)

defint(f,t,0,2*pi)
```
@Algebrite.eval



## Text Analysis

``` text  Trump, Presidential Bid announcement
Thank you. It’s true, and these are the best and the
finest. When Mexico sends its people, they’re not sending
their best. They’re not sending you. They’re not sending
you. They’re sending people that have lots of problems, and
they’re bringing those problems with us. They’re bringing
drugs. They’re bringing crime. They’re rapists. And some,
I assume, are good people.

But I speak to border guards and they tell us what we’re
getting. And it only makes common sense. It only makes
common sense. They’re sending us not the right people.
```
@Textanalysis.FULL

> Template: https://github.com/liaTemplates/TextAnalysis 


## Share your content 

### Using links

### Using Lia Exporter
