---
title: 'Tipo parcial: Referencia de C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- partialtype
- partialtype_CSharpKeyword
helpviewer_keywords:
- partial types [C#]
ms.assetid: 27320743-a22e-4c7b-b0b3-53afe3607334
ms.openlocfilehash: ed3e18c5981fa52dc2c6ef09bfb666cfa705fede
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239571"
---
# <a name="partial-type-c-reference"></a>Tipo parcial (Referencia de C#)

Las definiciones de tipo parcial permiten dividir la definición de una clase, estructura o interfaz en varios archivos.

En *File1.cs*:

[!code-csharp[csrefKeywordsContextual#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#3)]  

La declaración en *File2.cs*:

[!code-csharp[csrefKeywordsContextual#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#4)]  

## <a name="remarks"></a>Comentarios

Dividir un tipo de clase, estructura o interfaz en varios archivos puede resultar útil cuando trabaja con proyectos de gran tamaño o con código generado automáticamente, como el proporcionado por el [Diseñador de Windows Forms](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md). Un tipo parcial puede contener un [método parcial](partial-method.md). Para más información, vea [Clases y métodos parciales](../../programming-guide/classes-and-structs/partial-classes-and-methods.md).

## <a name="c-language-specification"></a>Especificación del lenguaje C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Vea también

- [Referencia de C#](../index.md)
- [Guía de programación de C#](../../programming-guide/index.md)
- [Modificadores](modifiers.md)
- [Introducción a los genéricos](../../programming-guide/generics/introduction-to-generics.md)