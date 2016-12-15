---
title: "C&#243;mo: Agrupar resultados por claves contiguas (Gu&#237;a de programaci&#243;n de C#) | Microsoft Docs"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "claves contiguas [LINQ en C#]"
ms.assetid: 0f0f48a8-e13b-4274-8903-3b73f68cd18e
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# C&#243;mo: Agrupar resultados por claves contiguas (Gu&#237;a de programaci&#243;n de C#)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

En el siguiente ejemplo se muestra cómo agrupar elementos en fragmentos que representan secuencias secundarias de claves contiguas.  Por ejemplo, suponga que se le proporciona la siguiente secuencia de pares clave\-valor:  
  
|Clave|Valor|  
|-----------|-----------|  
|A|Nosotros|  
|A|creemos|  
|A|que|  
|B|Linq|  
|C|es|  
|A|realmente|  
|B|interesante|  
|B|\!|  
  
 Se crearán los siguientes grupos en este orden:  
  
1.  Nosotros, creemos, que  
  
2.  Linq  
  
3.  es  
  
4.  realmente  
  
5.  interesante, \!  
  
 La solución se implementa como un método de extensión seguro para subprocesos que devuelve sus resultados mediante transmisión por secuencias.  Es decir, genera sus grupos a medida que se desplaza por la secuencia de origen.  A diferencia de los operadores `group` u `orderby`, puede comenzar a devolver grupos al llamador antes de que se haya leído toda la secuencia.  
  
 Para que los subprocesos sean seguros, se realiza una copia de cada grupo o fragmento a medida que se recorre en iteración la secuencia de origen, tal y como se explica en los comentarios del código fuente.  Si la secuencia de origen tiene una secuencia grande de elementos contiguos, Common Language Runtime puede producir una excepción <xref:System.OutOfMemoryException>.  
  
## Ejemplo  
 En el siguiente ejemplo se muestran el método de extensión y el código de cliente que lo utiliza.  
  
 [!code-cs[cscsrefContiguousGroups#1](../../../csharp/programming-guide/linq-query-expressions/codesnippet/CSharp/how-to-group-results-by-contiguous-keys_1.cs)]  
  
 Para utilizar el método de extensión en su proyecto, copie la clase estática `MyExtensions` en un archivo de código fuente nuevo o ya existente y, si es necesario, agregue una directiva `using` para el espacio de nombres donde se encuentra.  
  
## Vea también  
 [Expresiones de consulta LINQ](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [Classification of Standard Query Operators by Manner of Execution](../../../visual-basic/programming-guide/concepts/linq/classification-of-standard-query-operators-by-manner-of-execution.md)