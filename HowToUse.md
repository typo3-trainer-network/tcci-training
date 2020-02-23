# How to use 

Syntax for the file Slides.md

## Add a new slide

With three dashes `---` a new slide is added.

This is followed by the unique identifier `name:` that is also used for internal links.
With the specification `class:` the layout of the slide can be specified.


### Example:
```markdown
---
name: identifier-for-the-slide
class: h1-fullwidth

# Header

## Subheader

* List item 1
* List item 2
* List item 3
* List item ...
```

## Add a new step for the current slide 

With two dashes `--` the presentation will wait for a click to show the next thing

### Example:
```markdown
---
name: identifier-for-the-slide-2
class: h1-fullwidth

# Header

--

* List item 1

--

* List item 2

--

* List item 3

--

* ...
```



## Available layouts

### .h1-fullwidth
The standard layout for slides
    
### .fullscreen-image
A layout with a fullscreen background-image
The background image must be added with
`background-image: url(../../images/my-image-file.png)`
    
#### Positioning for layout "fullscreen-image"

The classes center and right are used for text alignment.

### .fullscreen-image-pos-absolute

#### Example:

```markdown
.pa.r-10p.t-45p[
    The text is aligned 10% from the right and 45% from the top.
]
```

### Smaller font size

If you need the font-size smaller, you can add the CSS class `small` and/or `question`

The class `small` change the font size for continuous text (p, li).

The class `question` change the font size for the HTML tag h2. This class should always be used for questions and answers.

## Positioning
Absolute positioning is possible with the class `.pa`

The classes use the format:
[side]-[amount]p

The side can have the values:

* l (left)
* r (right)
* t (top)

The percent amount is an integer with values between 5-30 for left and right and 5-95 for top. (in 5% steps)

.l-20p in the markdown file corresponds to the CSS
 ```css
.l-20p {left: 20%}
 ```




## Colors:

You can use the classes __.blue, .green, .red, .orange , .yellow, .black, .white__ for text color.

### Syntax:

```markdown
.blue[Here is the blue text.]
```

---
## Footnotes

A footnote can be added with the class .footnote

### Example for a footnote with a red asterix
```
.footnote[.red.bold[*]
Important footnote]
```


