---
title: "Demasiados archivos | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.topic: "article"
f1_keywords: 
  - "vbrID67"
dev_langs: 
  - "VB"
ms.assetid: 2ff203e2-bba6-43ae-b72f-8e92a881c98f
caps.latest.revision: 7
author: "stevehoag"
ms.author: "shoag"
caps.handback.revision: 7
---
# Demasiados archivos
[!INCLUDE[vs2017banner](../../../visual-basic/developing-apps/includes/vs2017banner.md)]

O se han creado más archivos en el directorio raíz de los que permite el sistema operativo, o se han abierto más archivos que el número especificado en la configuración **files\=** del archivo CONFIG.SYS.  
  
### Para corregir este error  
  
1.  Si el programa abre, cierra o guarda archivos en el directorio raíz, modifique el programa para que utilice un subdirectorio.  
  
2.  Aumente el número de archivos especificado en la configuración **files\=** del archivo CONFIG.SYS y reinicie el equipo.  
  
## Vea también  
 [Tipos de error](../../../visual-basic/programming-guide/language-features/error-types.md)