---
Title: Generative Content
collection: touchdesigner
permalink: /Generative-Content/
toc: true
header:
  overlay_image: /assets/images/Generative-Header.jpg
  overlay_filter: 0.25
  show_overlay_excerpt: false
sidebar:
    nav: 'side'
---
Recopilatorio de técnicas para generar contenido con Touchdesigner.  
En un principio utilizo una clasificación realizada por [Simon Alexander](https://www.simonaa.media/tutorials/daily-practice){:target="_blank"}.  
Aunque iré completando según encuentre nuevos tutoriales y procedimientos y no pueda encuadrarlos en esta clasificación.

## Looping Noise:
Generar loops de videos donde operadores de `noise` generan estos loops aleatorios.  

_Links:_  
    - [Make some noise de Mathew Ragan](https://matthewragan.com/make-some-noise-sf-2017-touchdesigner/){:target="_blank"}    
    - [Generative Design – Shape and Noise de Mathew Ragan](https://matthewragan.com/2015/03/29/thp-494-598-generative-design-shape-and-noise-touchdesigner/){:target="_blank"}  
    - [Infinite Tunnel](https://www.simonaa.media/tutorials/looping-noise-part-2-infinite-tunnel-zoom){:target="_blank"}  
    - [End-begin](https://www.simonaa.media/tutorials/looping-noise-part-1){:target="_blank"}  
    - [Variable Line Width](https://www.simonaa.media/tutorials/line-width){:target="_blank"}  

## Reaction Diffusion: 
Dos compuestos o seres microscópicos reaccionando entre sí.  

> "Reaction diffusion is the simulation of two virtual chemicals reacting and diffusing on a 2D grid"

Como explica [Karl Sims][Karl Sims]{:target="_blank"}

_Links:_
- [Tutorial de Paketa12 sobre Reaction Diffusion][Paketa12]{:target="_blank"}  
- [Cellullar Noise by Elekktronaut][Elekktronaut - Cellullar Noise]{:target="_blank"} 


## Cellullar Automata: 
Una panal de celdas donde cambian en cada frame según una reglas preestablecidas.  

**Links:**    
- [Cellullar Automata de Darien Brito][Darien Brito]{:target="_blank"}   

## Space Filling Curves: 
Curvas que pasan a traves de cada punto de un cuadrado.  

[Link a explicación][3Blue1Brown]{:target="_blank"}

Another important resource is the book [“The Algorithmic Beauty of Plants” by Prusinkiewicz and Lindenmayer](/https://mega.nz/file/2rhB1bBK#f26G70M-Xhfwf1i0h-dXWogbjoXzQLlAf-zkdQWjZTs){:target="_blank"}, which contains many examples space of filling curves which can be ported to TouchDesigner’s L-System SOP.

[Toxes de David Braun - BeesandBombs, etc...][David Braun]{:target="_blank"}

## Shapes:
Lo más parecido al motion graphic típico. 
[Shapes en Generative Design][Generative Design]
[Simple VHS Animations - Elekktronaut](https://derivative.ca/community-post/tutorial/simple-vhs-animations/62763)

## Typo:

[Kinetic Typography - Serie de 3 tutoriales][KineticTypo]

## Flocking Boids:
> The idea is for individual objects to steer and align themselves to other objects. 

Igual que las bandadas de pájaros.
- [Flocking/Boids GPU tutorial][matthewwatcher]{:target="_blank"}  
![Flocking/Boids](https://forum.derivative.ca/uploads/default/original/2X/4/4e93cdf0a8157add954f9b903003f70d4eb06f2a.jpeg)
- [Compute Flocking][hardworkparty]{:target="_blank"}  

## Displacement and Pixel Sorting:

[Noise Displacement](https://www.simonaa.media/tutorials/noisedisplacement){:target="_blank"}    
[Inspired by Rutt Etra | TouchDesigner](https://matthewragan.com/2014/04/27/inspired-by-rutt-etra-touchdesigner/){:target="_blank"}  
[Pixel Sorting by Elecctronaut](https://derivative.ca/community-post/tutorial/pixel-sorting){:target="_blank"}

----------------------------------------------
[KineticTypo]: https://www.youtube.com/watch?v=zrA9gaCymjM&feature=youtu.be
[Paketa12]: https://www.facebook.com/watch/?v=1408728442564632
[Karl Sims]: http://www.karlsims.com/rd.html 
[Darien Brito]: https://derivative.ca/community-post/tutorial/cellular-automata-tutorial-series/62778
[3Blue1Brown]: https://www.youtube.com/watch?v=RU0wScIj36o
[David Braun]: https://github.com/DBraun/TouchDesigner_Shared
[matthewwatcher]: https://forum.derivative.ca/t/flocking-boids-gpu/8037
[hardworkparty]: https://forum.derivative.ca/t/compute-flocking/10408
[Generative Design]: https://docs.derivative.ca/Generative_Design  
[Elekktronaut - Cellullar Noise]: https://derivative.ca/community-post/tutorial/cellular-noise-instancing
