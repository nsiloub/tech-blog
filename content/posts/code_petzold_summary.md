---
title: "Code: The Hidden Language of Computer Hardware and Software - Charles Petzold"
# subtitle: "From electronic circuits and Boolean logic to processors and programs: a technical foundation of computer hardware and software"
date: 2026-03-22T17:00:30+01:00
lastmod: 2026-03-22T17:00:30+01:00
draft: false
author: ""
authorLink: ""
description: ""
license: ""
images: []

tags: ["Books Summary", Computer Architecture,]
categories: [Books Summary, Computer Architecture, "code - Charles Petzold"]

featuredImage: "articles/petzold/peztold-summary-009.svg"
featuredImagePreview: "articles/petzold/peztold-summary-009.svg"

hiddenFromHomePage: false
hiddenFromSearch: false
twemoji: false
lightgallery: true
ruby: true
fraction: true
fontawesome: true
linkToMarkdown: true
rssFullText: false

toc:
  enable: true
  auto: true
code:
  copy: true
  maxShownLines: 50
math:
  enable: false
  # ...
mapbox:
  # ...
share:
  enable: true
  # ...
comment:
  enable: true
  # ...
library:
  css:
    # someCSS = "some.css"
    # located in "assets/"
    # Or
    # someCSS = "https://cdn.example.com/some.css"
  js:
    # someJS = "some.js"
    # located in "assets/"
    # Or
    # someJS = "https://cdn.example.com/some.js"
seo:
  images: ["articles/petzold/peztold-summary-006"]
  thumbnailUrl: "articles/petzold/peztold-summary-009.svg"
  # ...
---

From electronic circuits and Boolean logic to processors and programs: a technical foundation of computer hardware and software.

<!--more-->

## Chapters 1 to 3
{{< mermaid >}}
    flowchart TB
        A[Situation 1: Flashlights] --> |Chapter 1|D([Morse Code])
        B[Code and Combinations] --> |Chapter 2|D([Morse Code])e1@==> F((Situational Languages))
        C[Situation 2: Can't see] --> |Chapter 3|E([Braille Code])e2@==> F((Situational Languages))e3@==> |Efficiency|G(Binary Systems)
        e1@{ animate: true }
        e2@{ animate: true }
        e3@{ animate: true }
{{< /mermaid >}}

 ### Situational languages

The first three chapters introduce the idea of what I call ***"situational languages"*** by showing that, for a given situation, different means of communication are employed; they also build the intuition about why a binary (two-state) system is best suited for those situational languages.      
<br>
The author starts with an example of two teenagers in separate houses whose rooms face one another. But they can't talk at night, and they only have flashlights. How will they communicate? Well, they could swing and wave their flashlights to write words. But soon they discover that the idea of drawing alphabetic letters in thin air doesn't seem very appealing or efficient.  
A more ingenious idea would be to use Morse code, where they only have combinations of short and long blinks, and then predefine some sequences and patterns and attach them to the known alphabetic letters.

| A | •− | J | •−−− | S | ••• |
|---:|:---|---:|:----|---:|:---|
| B | −••• | K | −•− | T | − |
| C | −•−• | L | •−•• | U | ••− |
| D | −•• | M | −− | V | •••− |
| E | • | N | −• | W | •−− |
| F | ••−• | O | −−− | X | −••− |
| G | −−• | P | •−−• | Y | −•−− |
| H | •••• | Q | −−•− | Z | −−•• |
| I | •• | R | •−• |   |    |



<br>
This is more efficient and suits that situation better, and they have a ready system to communicate at night with flashlights! 
<br>  

Another example of this "situational languages" would be about a blind person.
Let's say, hypothetically, that you were to communicate with that person, but for some reason you can't talk. The other person is able to use their fingers and understand something by touching it. So you could devise a system where you emboss each letter on a special piece of paper so that the other person can read words by touching them on the paper.  
This could work, but again, the idea of reading a full text one letter at a time does not seem very efficient.
A better idea would be to do what Braille did: devise a system that uses only two kinds of dots — a flat dot and a raised (embossed) dot — and, just like with Morse code, attach each alphabetic letter to a particular pattern of those flat/raised dots. You'd have something like this:



![Flat and embossed circles](articles/petzold/flat-embossed-000.svg)

| a | b | c | d | e | f | g | h | i | j |
|---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| ●○<br>○○<br>○○ | ●○<br>●○<br>○○ | ●●<br>○○<br>○○ | ●●<br>○●<br>○○ | ●○<br>○●<br>○○ | ●●<br>●○<br>○○ | ●●<br>●●<br>○○ | ●○<br>●●<br>○○ | ○●<br>●○<br>○○ | ○●<br>●●<br>○○ |

| k | l | m | n | o | p | q | r | s | t |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| ●○<br>○○<br>●○ | ●○<br>●○<br>●○ | ●●<br>○○<br>●○ | ●●<br>○●<br>●○ | ●○<br>○●<br>●○ | ●●<br>●○<br>●○ | ●●<br>●●<br>●○ | ●○<br>●●<br>●○ | ○●<br>●○<br>●○ | ○●<br>●●<br>●○ |

| u | v | w | x | y | z |
|:---:|:---:|:---:|:---:|:---:|:---:|
| ●○<br>○○<br>●● | ●○<br>●○<br>●● | ○●<br>●●<br>○○ | ●●<br>○○<br>●● | ●●<br>○●<br>●● | ●○<br>○●<br>●● |




### Why Binaries ?
By now you can see the pattern in these examples:

1.  We have a given situation: a known language that isn't suited for the situation;
2.  We devise a communication system best suited for that situation;
3.  We create some predefined sequences in that system;
4.  We attach or bind each alphabetic letter to a particular sequence.


![recap-steps](articles/petzold/diagrams/recap-steps-002.svg)


You can also see that all those "situational languages" use only two-state characters: a dot or a dash for Morse code; a flat or a raised circle for Braille, etc.
So now the big questions arise:

- Why do binaries seem so ubiquitous?
- What do they have to do with languages?  


There may be multiple factors, but the most evident and logical is: the more variables a system has, the less predictable and reliable it becomes, and the more confusion it introduces.
Relating this to our examples: imagine that for Morse code we introduced another blink length — a medium blink between short and long. How would we measure that medium blink? How would we differentiate it from the long one? Not only would communication become more confusing, but assigning patterns to the alphabet would be harder because there would be more states to manage. 
<br>
That is why a binary system is often the more viable fit: it's greater than 1 (so you can represent information) but not as complex as 3 or more states, making it more reliable and manageable. 
<br><br>



That was my take on the first three chapters. Read more in the next parts below
