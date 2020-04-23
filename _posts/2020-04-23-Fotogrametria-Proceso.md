---
title: Fotogrametria Resumen
tags:
    - fotogrametria
    - agisoft 
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

### 2. tie points (conexion entre las imagenes - puntos de referencias)
### 3. Depth Map
### 4. Dense cloud
### 5. Mesh 