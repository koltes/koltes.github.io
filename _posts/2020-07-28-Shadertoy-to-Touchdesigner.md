---
title: Shadertoy to Touchdesigner
categories:
  - Tutorial
tags:
    - glsl
sidebar:
    nav: 'side'  
---

# Pasos para adaptar un shadertoy a Touch

1. Cambiar `mainImage(out vec4 etc...)` por `main()`  
2. Insertar al principio:
`layout(location = 0) out vec4 fragColor;`  

3. Copiar los uniforms a continuación y configurarlos en la pestaña de vectors.
4. Descargar los samplers necesarios o sustituirlos.
    - 
4. Sustituir los samplers `iChannel*` por `sTD2DInputs[*]`.
    - Si fueran cubemaps sería `sTDCubeInputs[*]` y el numero de index no de las entradas totales sino de las entradas Cubemaps.


## Descargar samplers (Shadertoy API)

`https://www.shadertoy.com/api/v1/shaders/**SHADERid**?key=**NumeroAPIdemiusuario**`

En el codigo JSON que me aparece localizar inputs y copiar la ruta y pegarla detrás de: `https://www.shadertoy.com/ruta`