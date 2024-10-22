# Just enough Markdown

toc doesn't work

# Table of Contents
 [1.Headings](#1.Heading)   
 [2.HR](#2.HR)  
 [3.Bold, italic, emphasize text and line break](#3.Bold,-italic,-emphasize-text-and-line-break)  
 [4.Paragraphs](#4.Paragraphs)  
 [5.Blockquotes](#5.Blockquotes)  
 [6.Links, anchors and images](#6.Links,-anchors-and-images)  
 [7.Lists](#7.Lists)  
 [8.Code and escaping backtick](#8.Code-and-escaping-backtick)  
 [9.Other](#9.Other)  
 

### 1.Heading ###
---
\# Heading 1...6
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
---
### 2.HR ###
Horizontal line  
\---

---
### 3.Bold, italic, emphasize text and line break ###

This is \*\*bold\*\* text.  
This is \*\*\*italic\*\*\* text.  
This is \_\_\_emphasize\_\_\_ text.  
And this is line break \  .

This is **bold** text.  
This is ***italic*** text.  
This is ___emphasize___ text.

---
### 4.Paragraphs ###
Just blank line before and after line.


This is paragraph 1.

This is paragraph 2.

---
### 5.Blockquotes ###
\>This is blockquotes.  
 
\> And this is blockquotes 

\>

\> on three lines.    

>This is blockquotes.

> And this is blockquotes 
>  
> on three lines.  
---
### 6.Links, anchors and images ###
This is \[Github link\]\(https://github.com).  
This is image \!\[placeholder image\] (http://via.placeholder.com/100x100)  
\###anchor1\###   

\[link anchor1\]\(#anchor1\)  

This is [Github link](https://github.com).  
This is image ![placeholder image](http://via.placeholder.com/100x100/)  
Image in folder ![tux](assets/tux.png)  

### anchor1 ###  
[link anchor1](#anchor1) 

---
### 7.Lists ### 
Ordered lists  
1. item 1
2. item 2
    1. idented item1
    2. idented item 2
3. item 3
4. item 4

Unoredered lists

- item 1
- item 2
    + idented item 1
    * idented item 2
- item 3

### 8.Code and escaping backtick ###
html  

```html
   <html>
      <head>
      </head>
  </html>
  ```
python  

```python
import sympy as s
# comment
print("Hello, World!")


```
`this is "code"`

### 9.Other ###
Table
|one|two|three|
|---|---|-----|
|item|item|item|
|item|item|item|
|item|item|item|
|item|item|item|
  
Formulas:  
x<sub>1</sub>+x<sub>2</sub>  
x<sup>2</sup> + x<sup>2</sup> = 2*x<sup>2  

Checkbox:  
- [x] Milestone 1
- [ ] Milestone 2
- [x] Milestone 3
- [ ] Milestone 4
    
    
Latex:  
  inline  $\Phi^{2}+x=4$   
  display $$\Phi^{2}+x=4$$   
