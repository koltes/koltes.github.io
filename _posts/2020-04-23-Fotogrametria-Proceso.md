---
title: Fotogrametria Resumen
tags:
    - fotogrametria
    - metashape
categories:
    - tutorial
    - workflow  
sidebar:
    nav: 'side'
---
Siguiendo el sistema estudiado en Domestika.  
## Photoshop o Lightroom  
Procesos para equilibrar la imagen.  
1. White Balance   
2. Exposure  
3. Contrast  
4. Highlights  
5. Shadows    

## Agisoft  
### 0. Añadir fotos  
1. Workflow>Add photos  
2. Seleccionar todas>Estimate Image Quality `(RMB)`    
3. Las que estén por debajo de 0.5 deshecharlas.  

### 1. Alinear fotos  
1. Workflow > Align Images  
2. Align Selected Cameras `(RMB)`   
Fuerza a imagenes no procesadas a incluirlas también.  
> Apunte: **Máscaras**. En fotogrametría de estudio es bueno hacer una máscara de 1 imagen para quitar el fondo de la imagen. La mascara funciona pues la cámara no se ha movido y lo que ha rotado ha sido el objeto.
Este proceso se haría antes de Align Selected Cameras. 
  
3. Renombrar el chunk y guardar.  
4. Duplicar el chunk por si hubiera que volver atrás.  
 
##### 1.1 Optimizar cámaras
Tools > Optimizar cámaras

##### 1.2 Borrado de puntos defectuosos
1. Model > Gradual Selection
    - Reprojection Error (ajustar el slider para seleccionar algunos puntos)
    - Borrar puntos seleccionados.
2. Model > Gradual Selection
    + Reconstruction uncertainty

##### 1.3 Limpiar puntos
Limpiar nube de puntos a mano

### 2. Construir Nube de puntos
1. Workflow > Build Point Cloud
> Depth filtering: Agressive
2. Limpiar puntos de nuevo.

### 3. Construir Mesh y textura
1. Workflow > Mesh
    + Surface Type: Arbitrary - Si la superficie no es plana. Si no, escoger Height Field para superficies planas.   
    + Face count: Numero de poligonos que crea.

##### 3.1 Reducir poligonaje (Decimation)
1. Tools > Mesh > Decimation Mesh
> Le decimos el numero de poligonos con los que trabajar.







--------------------
