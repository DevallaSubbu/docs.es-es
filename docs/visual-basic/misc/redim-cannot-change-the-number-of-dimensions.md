---
title: "&#39;ReDim&#39; no puede cambiar el n&#250;mero de dimensiones. | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-visual-basic"
ms.topic: "article"
f1_keywords: 
  - "vbrArray_RankMismatch"
ms.assetid: 52505298-9985-4682-8f6e-ff7d56077f34
caps.latest.revision: 9
author: "stevehoag"
ms.author: "shoag"
caps.handback.revision: 9
---
# &#39;ReDim&#39; no puede cambiar el n&#250;mero de dimensiones.
Una operación intenta usar la instrucción `ReDim` para cambiar el rango \(número de dimensiones\) de una matriz.`ReDim` puede cambiar el tamaño de una o más dimensiones de una matriz que ya se ha declarado formalmente, pero no puede cambiar el rango de la matriz.  
  
### Para corregir este error  
  
-   Asegúrese de que intenta cambiar el rango de la matriz y no los tamaños de sus dimensiones y, si es posible, use `Dim` para declarar una nueva matriz con el rango deseado.  
  
## Vea también  
 [NOTINBUILD Información general de matrices en Visual Basic](http://msdn.microsoft.com/es-es/ca50e2f2-b4d2-4c57-9169-9abbcc3392d8)   
 [NOTINBUILD Matrices multidimensionales en Visual Basic](http://msdn.microsoft.com/es-es/d92cad25-07e2-4d79-8ea4-ab269700f5de)   
 [ReDim \(Instrucción\)](../../visual-basic/language-reference/statements/redim-statement.md)   
 [Dim \(Instrucción\)](../../visual-basic/language-reference/statements/dim-statement.md)