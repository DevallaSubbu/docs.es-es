---
title: "Dominio de accesibilidad (Referencia de C#) | Microsoft Docs"
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
  - "dominio de accesibilidad [C#]"
ms.assetid: 8af779c1-275b-44be-a864-9edfbca71bcc
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Dominio de accesibilidad (Referencia de C#)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

El dominio de accesibilidad de un miembro especifica en qué secciones del programa se puede hacer referencia a dicho miembro.  Si el miembro está anidado dentro de otro tipo, su dominio de accesibilidad viene determinado por el [nivel de accesibilidad](../../../csharp/language-reference/keywords/accessibility-levels.md) del miembro y por el dominio de accesibilidad del tipo contenedor inmediato.  
  
 El dominio de accesibilidad de un tipo de nivel superior es por lo menos el texto del programa del proyecto en el que se declara.  Es decir, el dominio incluye todos los archivos de origen de este proyecto.  El dominio de accesibilidad de un tipo anidado es, al menos, el texto del programa en el que el tipo aparece declarado.  Es decir, el dominio es el cuerpo del tipo, que incluye todos los tipos anidados.  El dominio de accesibilidad de un tipo anidado no puede superar al del tipo contenedor.  Estos conceptos se muestran en el siguiente ejemplo.  
  
## Ejemplo  
 Este ejemplo contiene un tipo de nivel superior, `T1`, y dos clases anidadas, `M1` y `M2`.  Las clases contienen campos que tienen diferentes accesibilidades declaradas.  En el método `Main`, a cada instrucción le sigue un comentario que indica el dominio de accesibilidad de cada miembro.  Observe que las instrucciones que intentan hacer referencia a los miembros inaccesibles están marcadas con comentarios.  Si desea ver los errores generados por el compilador cuando se intenta hacer referencia a un miembro inaccesible, quite los comentarios de uno en uno.  
  
 [!code-cs[csrefKeywordsModifiers#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/accessibility-domain_1.cs)]  
  
## Especificación del lenguaje C\#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Vea también  
 [Referencia de C\#](../../../csharp/language-reference/index.md)   
 [Guía de programación de C\#](../../../csharp/programming-guide/index.md)   
 [Palabras clave de C\#](../../../csharp/language-reference/keywords/index.md)   
 [Modificadores de acceso](../../../csharp/language-reference/keywords/access-modifiers.md)   
 [Niveles de accesibilidad](../../../csharp/language-reference/keywords/accessibility-levels.md)   
 [Restricciones en el uso de los niveles de accesibilidad](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md)   
 [Modificadores de acceso](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)   
 [public](../../../csharp/language-reference/keywords/public.md)   
 [private](../../../csharp/language-reference/keywords/private.md)   
 [protected](../../../csharp/language-reference/keywords/protected.md)   
 [internal](../../../csharp/language-reference/keywords/internal.md)