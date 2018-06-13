---
title: 'Instrucciones de formato de código de F #'
description: 'Obtenga información acerca de las directrices para dar formato al código de F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 6c8e4059fd4bf1e7450118a6df02609217c4f4db
ms.sourcegitcommit: 2ad7d06f4f469b5d8a5280ac0e0289a81867fc8e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2018
ms.locfileid: "35231517"
---
# <a name="f-code-formatting-guidelines"></a><span data-ttu-id="da824-103">Instrucciones de formato de código de F #</span><span class="sxs-lookup"><span data-stu-id="da824-103">F# code formatting guidelines</span></span>

<span data-ttu-id="da824-104">Este artículo proporciona instrucciones acerca de cómo aplicar formato al código para que el código de F # es:</span><span class="sxs-lookup"><span data-stu-id="da824-104">This article offers guidelines for how to format your code so that your F# code is:</span></span>

* <span data-ttu-id="da824-105">Generalmente se visualiza como más legible</span><span class="sxs-lookup"><span data-stu-id="da824-105">Generally viewed as more legible</span></span>
* <span data-ttu-id="da824-106">Está de acuerdo con convenciones aplicadas dando formato a otros editores y herramientas en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="da824-106">Is in accordance with conventions applied by formatting tools in Visual Studio and other editors</span></span>
* <span data-ttu-id="da824-107">Similar a otro código en línea</span><span class="sxs-lookup"><span data-stu-id="da824-107">Similar to other code online</span></span>

<span data-ttu-id="da824-108">Estas instrucciones se basan en [una guía completa para las convenciones de formato de F #](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) por [Phan Anh estiércol](https://github.com/dungpa).</span><span class="sxs-lookup"><span data-stu-id="da824-108">These guidelines are based on [A comprehensive guide to F# Formatting Conventions](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) by [Anh-Dung Phan](https://github.com/dungpa).</span></span>

## <a name="general-rules-for-indentation"></a><span data-ttu-id="da824-109">Reglas generales para la sangría</span><span class="sxs-lookup"><span data-stu-id="da824-109">General rules for indentation</span></span>

<span data-ttu-id="da824-110">F # utiliza espacios en blanco significativos de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="da824-110">F# uses significant whitespace by default.</span></span> <span data-ttu-id="da824-111">Las instrucciones siguientes están diseñadas para proporcionar una orientación acerca de cómo hacer juegos malabares con algunos de los desafíos que esto puede imponer.</span><span class="sxs-lookup"><span data-stu-id="da824-111">The following guidelines are intended to provide guidance as to how to juggle some challenges this can impose.</span></span>

### <a name="using-spaces"></a><span data-ttu-id="da824-112">Con espacios</span><span class="sxs-lookup"><span data-stu-id="da824-112">Using spaces</span></span>

<span data-ttu-id="da824-113">Cuando es necesario aplicar sangría, debe usar espacios, no tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="da824-113">When indentation is required, you must use spaces, not tabs.</span></span> <span data-ttu-id="da824-114">Se requiere al menos un espacio.</span><span class="sxs-lookup"><span data-stu-id="da824-114">At least one space is required.</span></span> <span data-ttu-id="da824-115">Su organización puede crear los estándares de codificación para especificar el número de espacios que se utilizarán para la sangría; dos, tres o cuatro espacios de sangría en cada nivel donde se produce la sangría es normal.</span><span class="sxs-lookup"><span data-stu-id="da824-115">Your organization can create coding standards to specify the number of spaces to use for indentation; two, three or four spaces of indentation at each level where indentation occurs is typical.</span></span>

<span data-ttu-id="da824-116">**Se recomienda 4 espacios por sangría.**</span><span class="sxs-lookup"><span data-stu-id="da824-116">**We recommend 4 spaces per indentation.**</span></span>

<span data-ttu-id="da824-117">Es decir, sangría de programas es una cuestión subjetiva.</span><span class="sxs-lookup"><span data-stu-id="da824-117">That said, indentation of programs is a subjective matter.</span></span> <span data-ttu-id="da824-118">Variaciones están bien, pero es la primera regla que debería seguir *coherencia de sangría*.</span><span class="sxs-lookup"><span data-stu-id="da824-118">Variations are OK, but the first rule you should follow is *consistency of indentation*.</span></span> <span data-ttu-id="da824-119">Elija un estilo de sangría generalmente aceptado y usarlo de forma sistemática en todo el código base.</span><span class="sxs-lookup"><span data-stu-id="da824-119">Choose a generally accepted style of indentation and use it systematically throughout your codebase.</span></span>

## <a name="formatting-blank-lines"></a><span data-ttu-id="da824-120">Aplicar formato a líneas en blanco</span><span class="sxs-lookup"><span data-stu-id="da824-120">Formatting blank lines</span></span>

* <span data-ttu-id="da824-121">Independiente nivel superior (función) y la clase de definiciones con dos líneas en blanco.</span><span class="sxs-lookup"><span data-stu-id="da824-121">Separate top-level function and class definitions with two blank lines.</span></span>
* <span data-ttu-id="da824-122">Definiciones de método dentro de una clase se separan mediante una sola línea en blanco.</span><span class="sxs-lookup"><span data-stu-id="da824-122">Method definitions inside a class are separated by a single blank line.</span></span>
* <span data-ttu-id="da824-123">Líneas en blanco adicionales pueden usarse (con moderación) para separar los grupos de funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="da824-123">Extra blank lines may be used (sparingly) to separate groups of related functions.</span></span> <span data-ttu-id="da824-124">Pueden omitir las líneas en blanco entre una serie de líneas de código relacionados (por ejemplo, un conjunto de implementaciones ficticias).</span><span class="sxs-lookup"><span data-stu-id="da824-124">Blank lines may be omitted between a bunch of related one-liners (for example, a set of dummy implementations).</span></span>
* <span data-ttu-id="da824-125">Utilice las líneas en blanco en las funciones, con moderación, para indicar secciones lógicas.</span><span class="sxs-lookup"><span data-stu-id="da824-125">Use blank lines in functions, sparingly, to indicate logical sections.</span></span>

## <a name="formatting-comments"></a><span data-ttu-id="da824-126">Aplicar formato a los comentarios</span><span class="sxs-lookup"><span data-stu-id="da824-126">Formatting comments</span></span>

<span data-ttu-id="da824-127">Por lo general preferir múltiples comentarios de barra diagonal doble comentarios del bloque de estilo de aprendizaje automático.</span><span class="sxs-lookup"><span data-stu-id="da824-127">Generally prefer multiple double-slash comments over ML-style block comments.</span></span>

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

<span data-ttu-id="da824-128">Comentarios en línea deben poner en mayúscula la primera letra.</span><span class="sxs-lookup"><span data-stu-id="da824-128">Inline comments should capitalize the first letter.</span></span>

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a><span data-ttu-id="da824-129">Convenciones de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="da824-129">Naming conventions</span></span>

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a><span data-ttu-id="da824-130">Usar camelCase para funciones y los valores de límite de clase, expresión enlazados y límite de patrón</span><span class="sxs-lookup"><span data-stu-id="da824-130">Use camelCase for class-bound, expression-bound and pattern-bound values and functions</span></span>

<span data-ttu-id="da824-131">Es normal y aceptado estilo de F # que se usará camelCase para todos los nombres enlazados como variables locales o en coincidencias de patrón y las definiciones de función.</span><span class="sxs-lookup"><span data-stu-id="da824-131">It is common and accepted F# style to use camelCase for all names bound as local variables or in pattern matches and function definitions.</span></span>

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

<span data-ttu-id="da824-132">Las funciones enlazadas a localmente en clases también deben usar camelCase.</span><span class="sxs-lookup"><span data-stu-id="da824-132">Locally-bound functions in classes should also use camelCase.</span></span>

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a><span data-ttu-id="da824-133">Usar camelCase para funciones públicas de límite de módulo</span><span class="sxs-lookup"><span data-stu-id="da824-133">Use camelCase for module-bound public functions</span></span>

<span data-ttu-id="da824-134">Cuando una función de módulo enlazada es parte de una API pública, debe utilizar camelCase:</span><span class="sxs-lookup"><span data-stu-id="da824-134">When a module-bound function is part of a public API, it should use camelCase:</span></span>

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a><span data-ttu-id="da824-135">Usar camelCase para las funciones y los valores de límite de módulo privados e internos</span><span class="sxs-lookup"><span data-stu-id="da824-135">Use camelCase for internal and private module-bound values and functions</span></span>

<span data-ttu-id="da824-136">Use camelCase para los valores de límite de módulo privados, incluidas las siguientes:</span><span class="sxs-lookup"><span data-stu-id="da824-136">Use camelCase for private module-bound values, including the following:</span></span>

* <span data-ttu-id="da824-137">Funciones ad hoc en secuencias de comandos</span><span class="sxs-lookup"><span data-stu-id="da824-137">Ad hoc functions in scripts</span></span>

* <span data-ttu-id="da824-138">Valores que conforman la implementación interna de un tipo o módulo</span><span class="sxs-lookup"><span data-stu-id="da824-138">Values making up the internal implementation of a module or type</span></span>

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a><span data-ttu-id="da824-139">Usar camelCase para los parámetros</span><span class="sxs-lookup"><span data-stu-id="da824-139">Use camelCase for parameters</span></span>

<span data-ttu-id="da824-140">Todos los parámetros deben usar camelCase según las convenciones de nomenclatura. NET.</span><span class="sxs-lookup"><span data-stu-id="da824-140">All parameters should use camelCase in accordance with .NET naming conventions.</span></span>

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a><span data-ttu-id="da824-141">Utilizar PascalCase para módulos</span><span class="sxs-lookup"><span data-stu-id="da824-141">Use PascalCase for modules</span></span>

<span data-ttu-id="da824-142">Todos los módulos (nivel superior, internos, privados, anidados) deben usar PascalCase.</span><span class="sxs-lookup"><span data-stu-id="da824-142">All modules (top-level, internal, private, nested) should use PascalCase.</span></span>

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a><span data-ttu-id="da824-143">Usar PascalCase de declaraciones de tipos, miembros y etiquetas</span><span class="sxs-lookup"><span data-stu-id="da824-143">Use PascalCase for type declarations, members, and labels</span></span>

<span data-ttu-id="da824-144">Las clases, interfaces, estructuras, enumeraciones, delegados, registros y uniones discriminadas deben denominarse con PascalCase.</span><span class="sxs-lookup"><span data-stu-id="da824-144">Classes, interfaces, structs, enumerations, delegates, records, and discriminated unions should all be named with PascalCase.</span></span> <span data-ttu-id="da824-145">Los miembros dentro de los tipos y las etiquetas para los registros y uniones discriminadas también deben usar PascalCase.</span><span class="sxs-lookup"><span data-stu-id="da824-145">Members within types and labels for records and discriminated unions should also use PascalCase.</span></span>

```fsharp
type IMyInterface =
    abstract Something: int

type MyClass() =
    member this.MyMethod(x, y) = x + y

type MyRecord = { IntVal: int; StringVal: string }

type SchoolPerson =
    | Professor
    | Student
    | Advisor
    | Administrator
```

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a><span data-ttu-id="da824-146">Utilizar PascalCase para construcciones intrínsecas de .NET</span><span class="sxs-lookup"><span data-stu-id="da824-146">Use PascalCase for constructs intrinsic to .NET</span></span>

<span data-ttu-id="da824-147">Espacios de nombres, excepciones, eventos y el proyecto /`.dll` nombres también deben utilizar PascalCase.</span><span class="sxs-lookup"><span data-stu-id="da824-147">Namespaces, exceptions, events, and project/`.dll` names should also use PascalCase.</span></span> <span data-ttu-id="da824-148">No sólo hace esto que el consumo de otros lenguajes .NET sentirse más natural a los consumidores, también es coherente con las convenciones de nomenclatura de .NET que es probable que encuentre.</span><span class="sxs-lookup"><span data-stu-id="da824-148">Not only does this make consumption from other .NET languages feel more natural to consumers, it's also consistent with .NET naming conventions that you are likely to encounter.</span></span>

### <a name="avoid-underscores-in-names"></a><span data-ttu-id="da824-149">Evite los caracteres de subrayado en nombres</span><span class="sxs-lookup"><span data-stu-id="da824-149">Avoid underscores in names</span></span>

<span data-ttu-id="da824-150">Históricamente, algunas bibliotecas de F # usan caracteres de subrayado en nombres.</span><span class="sxs-lookup"><span data-stu-id="da824-150">Historically, some F# libraries have used underscores in names.</span></span> <span data-ttu-id="da824-151">Sin embargo, esto se ampliamente ya no se acepta, en parte porque entra en conflicto con las convenciones de nomenclatura. NET.</span><span class="sxs-lookup"><span data-stu-id="da824-151">However, this is no longer widely accepted, partly because it clashes with .NET naming conventions.</span></span> <span data-ttu-id="da824-152">Es decir, algunos programadores de F # utilizan caracteres de subrayado mucho, en parte por motivos históricos y respeto y la tolerancia es importante.</span><span class="sxs-lookup"><span data-stu-id="da824-152">That said, some F# programmers use underscores heavily, partly for historical reasons, and tolerance and respect is important.</span></span> <span data-ttu-id="da824-153">Sin embargo, tenga en cuenta que el estilo a menudo se disliked por otros usuarios que tienen una opción sobre si desea usarlo.</span><span class="sxs-lookup"><span data-stu-id="da824-153">However, be aware that the style is often disliked by others who have a choice about whether to use it.</span></span>

<span data-ttu-id="da824-154">Algunas excepciones incluye interoperar con componentes nativos, donde el carácter de subrayado es muy comunes.</span><span class="sxs-lookup"><span data-stu-id="da824-154">Some exceptions includes interoperating with native components, where underscores are very common.</span></span>

### <a name="use-standard-f-operators"></a><span data-ttu-id="da824-155">Utilizar operadores estándar de F #</span><span class="sxs-lookup"><span data-stu-id="da824-155">Use standard F# operators</span></span>

<span data-ttu-id="da824-156">Los operadores siguientes se definen en la biblioteca estándar de F # y deben utilizarse en lugar de definir equivalentes.</span><span class="sxs-lookup"><span data-stu-id="da824-156">The following operators are defined in the F# standard library and should be used instead of defining equivalents.</span></span> <span data-ttu-id="da824-157">Uso de estos operadores se recomienda tiende a dificultar el código sea más legible e idiomática.</span><span class="sxs-lookup"><span data-stu-id="da824-157">Using these operators is recommended as it tends to make code more readable and idiomatic.</span></span> <span data-ttu-id="da824-158">Los desarrolladores con un fondo en OCaml o en otro lenguaje de programación funcional pueden ser acostumbrados a diferentes expresiones.</span><span class="sxs-lookup"><span data-stu-id="da824-158">Developers with a background in OCaml or other functional programming language may be accustomed to different idioms.</span></span> <span data-ttu-id="da824-159">En la lista siguiente se resume los operadores de F # recomendados.</span><span class="sxs-lookup"><span data-stu-id="da824-159">The following list summarizes the recommended F# operators.</span></span>

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Discard away a value
x + y // Overloaded addition (including string concatenation)
x - y // Overloaded subtraction
x * y // Overloaded multiplication
x / y // Overloaded division
x % y // Overloaded modulus
x && y // Lazy/short-cut "and"
x || y // Lazy/short-cut "or"
x <<< y // Bitwise left shift
x >>> y // Bitwise right shift
x ||| y // Bitwise or, also for working with “flags” enumeration
x &&& y // Bitwise and, also for working with “flags” enumeration
x ^^^ y // Bitwise xor, also for working with “flags” enumeration
```

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a><span data-ttu-id="da824-160">Use la sintaxis de prefijo para los tipos genéricos (`Foo<T>`) con preferencia a sintaxis de postfijo (`T Foo`)</span><span class="sxs-lookup"><span data-stu-id="da824-160">Use prefix syntax for generics (`Foo<T>`) in preference to postfix syntax (`T Foo`)</span></span>

<span data-ttu-id="da824-161">F # hereda tanto el estilo de aprendizaje automático de postfijo de asignación de nombres de tipos genéricos (por ejemplo, `int list`), así como el estilo de .NET de prefijo (por ejemplo, `list<int>`).</span><span class="sxs-lookup"><span data-stu-id="da824-161">F# inherits both the postfix ML style of naming generic types (for example, `int list`) as well as the prefix .NET style (for example, `list<int>`).</span></span> <span data-ttu-id="da824-162">Prefiere el estilo. NET, excepto los cuatro tipos específicos:</span><span class="sxs-lookup"><span data-stu-id="da824-162">Prefer the .NET style, except for four specific types:</span></span>

1. <span data-ttu-id="da824-163">Para F # listas, utilice la forma de postfijo: `int list` en lugar de `list<int>`.</span><span class="sxs-lookup"><span data-stu-id="da824-163">For F# Lists, use the postfix form: `int list` rather than `list<int>`.</span></span>
2. <span data-ttu-id="da824-164">Para opciones de F #, utilice la forma de postfijo: `int option` en lugar de `option<int>`.</span><span class="sxs-lookup"><span data-stu-id="da824-164">For F# Options, use the postfix form: `int option` rather than `option<int>`.</span></span>
3. <span data-ttu-id="da824-165">Para las matrices de F #, utilice el nombre sintáctico `int[]` en lugar de `int array` o `array<int>`.</span><span class="sxs-lookup"><span data-stu-id="da824-165">For F# arrays, use the syntactic name `int[]` rather than `int array` or `array<int>`.</span></span>
4. <span data-ttu-id="da824-166">Para las celdas de referencia, utilice `int ref` en lugar de `ref<int>` o `Ref<int>`.</span><span class="sxs-lookup"><span data-stu-id="da824-166">For Reference Cells, use `int ref` rather than `ref<int>` or `Ref<int>`.</span></span>

<span data-ttu-id="da824-167">Para todos los otros tipos, utilice la forma de prefijo.</span><span class="sxs-lookup"><span data-stu-id="da824-167">For all other types, use the prefix form.</span></span>

## <a name="formatting-discriminated-union-declarations"></a><span data-ttu-id="da824-168">Formato discriminada declaraciones de unión</span><span class="sxs-lookup"><span data-stu-id="da824-168">Formatting discriminated union declarations</span></span>

<span data-ttu-id="da824-169">Aplicar sangría `|` en la definición de tipo por 4 espacios:</span><span class="sxs-lookup"><span data-stu-id="da824-169">Indent `|` in type definition by 4 spaces:</span></span>

```fsharp
// OK
type Volume =
    | Liter of float
    | FluidOunce of float
    | ImperialPint of float

// Not OK
type Volume =
| Liter of float
| USPint of float
| ImperialPint of float
```

<span data-ttu-id="da824-170">Uniones discriminadas instancias que se dividen en varias líneas debe proporcionar datos contenidos en un nuevo ámbito con sangría:</span><span class="sxs-lookup"><span data-stu-id="da824-170">Instantiated Discriminated Unions that split across multiple lines should give contained data a new scope with indentation:</span></span>

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

<span data-ttu-id="da824-171">También puede ser el paréntesis de cierre en una nueva línea:</span><span class="sxs-lookup"><span data-stu-id="da824-171">The closing parenthesis can also be on a new line:</span></span>

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-tuples"></a><span data-ttu-id="da824-172">Formato tuplas</span><span class="sxs-lookup"><span data-stu-id="da824-172">Formatting tuples</span></span>

<span data-ttu-id="da824-173">La creación de instancias de una tupla debe ir entre paréntesis, y las comas dentro de delimitadores deben ir seguidas un único espacio, por ejemplo: `(1, 2)`, `(x, y, z)`.</span><span class="sxs-lookup"><span data-stu-id="da824-173">A tuple instantiation should be parenthesized, and the delimiting commas within should be followed by a single space, for example: `(1, 2)`, `(x, y, z)`.</span></span>

<span data-ttu-id="da824-174">Una excepción aceptada es omitir los paréntesis en la coincidencia de patrones de tuplas:</span><span class="sxs-lookup"><span data-stu-id="da824-174">A commonly accepted exception is to omit parentheses in pattern matching of tuples:</span></span>

```fsharp
let (x, y) = z // Destructuring

match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-records"></a><span data-ttu-id="da824-175">Formato de registros</span><span class="sxs-lookup"><span data-stu-id="da824-175">Formatting records</span></span>

<span data-ttu-id="da824-176">Registros cortos pueden escribirse en una sola línea:</span><span class="sxs-lookup"><span data-stu-id="da824-176">Short records can be written in one line:</span></span>

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

<span data-ttu-id="da824-177">Los registros que tengan más deben usar nuevas líneas para etiquetas:</span><span class="sxs-lookup"><span data-stu-id="da824-177">Records that are longer should use new lines for labels:</span></span>

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

<span data-ttu-id="da824-178">Colocar el símbolo (token) de apertura en la misma línea y el símbolo (token) de cierre en una nueva línea también está bien:</span><span class="sxs-lookup"><span data-stu-id="da824-178">Placing the opening token on the same line and the closing token on a new line is also fine:</span></span>

```fsharp
let rainbow = {
    Boss1 = "Jeffrey"
    Boss2 = "Jeffrey"
    Boss3 = "Jeffrey"
    Boss4 = "Jeffrey"
    Boss5 = "Jeffrey"
    Boss6 = "Jeffrey"
    Boss7 = "Jeffrey"
    Boss8 = "Jeffrey"
    Lackeys = ["Zippy"; "George"; "Bungle"]
}
```

<span data-ttu-id="da824-179">Se aplican las mismas reglas para los elementos de lista y matriz.</span><span class="sxs-lookup"><span data-stu-id="da824-179">The same rules apply for list and array elements.</span></span>

## <a name="formatting-lists-and-arrays"></a><span data-ttu-id="da824-180">Aplicar formato a las listas y matrices</span><span class="sxs-lookup"><span data-stu-id="da824-180">Formatting lists and arrays</span></span>

<span data-ttu-id="da824-181">Escribir `x :: l` con espacios alrededor del `::` operador (`::` es un operador infijo, por lo tanto, rodeado por espacios) y `[1; 2; 3]` (`;` es un delimitador, por lo tanto, seguido por un espacio).</span><span class="sxs-lookup"><span data-stu-id="da824-181">Write `x :: l` with spaces around the `::` operator (`::` is an infix operator, hence surrounded by spaces) and `[1; 2; 3]` (`;` is a delimiter, hence followed by a space).</span></span>

<span data-ttu-id="da824-182">Utilice siempre al menos un espacio entre los dos operadores distintos de llave similar.</span><span class="sxs-lookup"><span data-stu-id="da824-182">Always use at least one space between two distinct brace-like operators.</span></span> <span data-ttu-id="da824-183">Por ejemplo, deje un espacio entre un `[` y `{`.</span><span class="sxs-lookup"><span data-stu-id="da824-183">For example, leave a space between a `[` and a `{`.</span></span>

```fsharp
// OK
[ { IngredientName = "Green beans"; Quantity = 250 }
  { IngredientName = "Pine nuts"; Quantity = 250 }
  { IngredientName = "Feta cheese"; Quantity = 250 }
  { IngredientName = "Olive oil"; Quantity = 10 }
  { IngredientName = "Lemon"; Quantity = 1 } ]

// Not OK
[{ IngredientName = "Green beans"; Quantity = 250 }
 { IngredientName = "Pine nuts"; Quantity = 250 }
 { IngredientName = "Feta cheese"; Quantity = 250 }
 { IngredientName = "Olive oil"; Quantity = 10 }
 { IngredientName = "Lemon"; Quantity = 1 }]
```

<span data-ttu-id="da824-184">Listas y matrices que se dividen en varias líneas siguen una regla similar igual que los registros:</span><span class="sxs-lookup"><span data-stu-id="da824-184">Lists and arrays that split across multiple lines follow a similar rule as records do:</span></span>

```fsharp
let pascalsTriangle = [|
    [|1|]
    [|1; 1|]
    [|1; 2; 1|]
    [|1; 3; 3; 1|]
    [|1; 4; 6; 4; 1|]
    [|1; 5; 10; 10; 5; 1|]
    [|1; 6; 15; 20; 15; 6; 1|]
    [|1; 7; 21; 35; 35; 21; 7; 1|]
    [|1; 8; 28; 56; 70; 56; 28; 8; 1|]
|]
```

## <a name="formatting-if-expressions"></a><span data-ttu-id="da824-185">Formato if expresiones</span><span class="sxs-lookup"><span data-stu-id="da824-185">Formatting if expressions</span></span>

<span data-ttu-id="da824-186">Sangría del condicionales depende de los tamaños de las expresiones que ellos constituyen.</span><span class="sxs-lookup"><span data-stu-id="da824-186">Indentation of conditionals depends on the sizes of the expressions that make them up.</span></span> <span data-ttu-id="da824-187">Si `cond`, `e1` y `e2` son pequeños, basta con escribirlos en una sola línea:</span><span class="sxs-lookup"><span data-stu-id="da824-187">If `cond`, `e1` and `e2` are small, simply write them on one line:</span></span>

```fsharp
if cond then e1 else e2
```

<span data-ttu-id="da824-188">Si `e1` y `cond` son pequeñas, pero `e2` es grande:</span><span class="sxs-lookup"><span data-stu-id="da824-188">If `e1` and `cond` are small, but `e2` is large:</span></span>

```fsharp
if cond then e1
else
    e2
```

<span data-ttu-id="da824-189">Si `e1` y `cond` son grandes y `e2` es pequeño:</span><span class="sxs-lookup"><span data-stu-id="da824-189">If `e1` and `cond` are large and `e2` is small:</span></span>

```fsharp
if cond then
    e1
else e2
```

<span data-ttu-id="da824-190">Si todas las expresiones son grandes:</span><span class="sxs-lookup"><span data-stu-id="da824-190">If all the expressions are large:</span></span>

```fsharp
if cond then
    e1
else
    e2
```

<span data-ttu-id="da824-191">Varias instrucciones condicionales con `elif` y `else` se les aplica sangría en el mismo ámbito que la `if`:</span><span class="sxs-lookup"><span data-stu-id="da824-191">Multiple conditionals with `elif` and `else` are indented at the same scope as the `if`:</span></span>

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a><span data-ttu-id="da824-192">Construcciones de búsqueda de coincidencias de patrón</span><span class="sxs-lookup"><span data-stu-id="da824-192">Pattern matching constructs</span></span>

<span data-ttu-id="da824-193">Use un `|` para cada cláusula de una coincidencia con ninguna sangría.</span><span class="sxs-lookup"><span data-stu-id="da824-193">Use a `|` for each clause of a match with no indentation.</span></span> <span data-ttu-id="da824-194">Si la expresión es corta, puede utilizar una sola línea si cada subexpresión también es sencilla.</span><span class="sxs-lookup"><span data-stu-id="da824-194">If the expression is short, you can consider using a single line if each subexpression is also simple.</span></span>

```fsharp
// OK
match l with
| { him = x; her = "Posh" } :: tail -> _
| _ :: tail -> findDavid tail
| [] -> failwith "Couldn't find David"

// Not OK
match l with
    | { him = x; her = "Posh" } :: tail -> _
    | _ :: tail -> findDavid tail
    | [] -> failwith "Couldn't find David"
```

<span data-ttu-id="da824-195">Si la expresión situada a la derecha de la flecha de coincidencia es demasiado grande, muévalo a la siguiente línea, con sangría un paso de la `match` / `|`.</span><span class="sxs-lookup"><span data-stu-id="da824-195">If the expression on the right of the pattern matching arrow is too large, move it to the following line, indented one step from the `match`/`|`.</span></span>

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

<span data-ttu-id="da824-196">Coincidencia de funciones anónimas, comenzando por `function`, por lo general debe no aplicar sangría demasiado lejos.</span><span class="sxs-lookup"><span data-stu-id="da824-196">Pattern matching of anonymous functions, starting by `function`, should generally not indent too far.</span></span> <span data-ttu-id="da824-197">Por ejemplo, está bien aplicar sangría a un ámbito como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="da824-197">For example, indenting one scope as follows is fine:</span></span>

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

<span data-ttu-id="da824-198">Patrón de búsqueda de coincidencias en las funciones definidas por `let` o `let rec` debe ser con sangría 4 espacios después de iniciar de `let`, incluso si `function` se utiliza la palabra clave:</span><span class="sxs-lookup"><span data-stu-id="da824-198">Pattern matching in functions defined by `let` or `let rec` should be indented 4 spaces after starting of `let`, even if `function` keyword is used:</span></span>

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

<span data-ttu-id="da824-199">No se recomienda alinear flechas.</span><span class="sxs-lookup"><span data-stu-id="da824-199">We do not recommend aligning arrows.</span></span>

## <a name="formatting-trywith-expressions"></a><span data-ttu-id="da824-200">Formato try / con expresiones</span><span class="sxs-lookup"><span data-stu-id="da824-200">Formatting try/with expressions</span></span>

<span data-ttu-id="da824-201">Coincidencia de patrones en el tipo de excepción deben aplicarse sangría en el mismo nivel que `with`.</span><span class="sxs-lookup"><span data-stu-id="da824-201">Pattern matching on the exception type should be indented at the same level as `with`.</span></span>

```fsharp
try
    if System.DateTime.Now.Second % 3 = 0 then
        raise (new System.Exception())
    else
        raise (new System.ApplicationException())
with
| :? System.ApplicationException ->
    printfn "A second that was not a multiple of 3"
| _ ->
    printfn "A second that was a multiple of 3"
```

## <a name="formatting-function-parameter-application"></a><span data-ttu-id="da824-202">Aplicación de parámetro de función de formato</span><span class="sxs-lookup"><span data-stu-id="da824-202">Formatting function parameter application</span></span>

<span data-ttu-id="da824-203">En general, la mayoría de los aplicaciones de parámetro de función se realiza en la misma línea.</span><span class="sxs-lookup"><span data-stu-id="da824-203">In general, most function parameter application is done on the same line.</span></span>

<span data-ttu-id="da824-204">Si desea aplicar parámetros a una función en una nueva línea, hágalo con un ámbito.</span><span class="sxs-lookup"><span data-stu-id="da824-204">If you wish to apply parameters to a function on a new line, indent them by one scope.</span></span>

```fsharp
// OK
sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
sprintf
     "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
let printVolumes x =
    printf "Volume in liters = %f, in us pints = %f, in imperial = %f"
        (convertVolumeToLiter x)
        (convertVolumeUSPint x)
        (convertVolumeImperialPint x)
```

<span data-ttu-id="da824-205">Se aplican las mismas directrices para las expresiones lambda como argumentos de función.</span><span class="sxs-lookup"><span data-stu-id="da824-205">The same guidelines apply for lambda expressions as function arguments.</span></span> <span data-ttu-id="da824-206">Si el cuerpo de una expresión lambda, el cuerpo puede tener otra línea, aplica sangría a un ámbito</span><span class="sxs-lookup"><span data-stu-id="da824-206">If the body of a lambda expression, the body can have another line, indented by one scope</span></span>

```fsharp
let printListWithOffset a list1 =
    List.iter
        (fun elem -> printfn "%d" (a + elem))
        list1

// OK if lambda body is long enough
let printListWithOffset a list1 =
    List.iter
        (fun elem ->
            printfn "%d" (a + elem))
        list1
```

<span data-ttu-id="da824-207">Sin embargo, si el cuerpo de una expresión lambda más de una línea, considere la posibilidad de factorización horizontal a una función diferente en lugar de tener una construcción de varias líneas aplicar como un solo argumento a una función.</span><span class="sxs-lookup"><span data-stu-id="da824-207">However, if the body of a lambda expression is more than one line, consider factoring it out into a separate function rather than have a multi-line construct applied as a single argument to a function.</span></span>

### <a name="formatting-infix-operators"></a><span data-ttu-id="da824-208">Aplicar formato a los operadores de infijo</span><span class="sxs-lookup"><span data-stu-id="da824-208">Formatting infix operators</span></span>

<span data-ttu-id="da824-209">Operadores separados por espacios.</span><span class="sxs-lookup"><span data-stu-id="da824-209">Separate operators by spaces.</span></span> <span data-ttu-id="da824-210">Obvias excepciones a esta regla son las `!` y `.` operadores.</span><span class="sxs-lookup"><span data-stu-id="da824-210">Obvious exceptions to this rule are the `!` and `.` operators.</span></span>

<span data-ttu-id="da824-211">Expresiones de infijo resulta adecuado para la línea en la misma columna:</span><span class="sxs-lookup"><span data-stu-id="da824-211">Infix expressions are OK to lineup on same column:</span></span>

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a><span data-ttu-id="da824-212">Aplicar formato a los operadores de canalización</span><span class="sxs-lookup"><span data-stu-id="da824-212">Formatting pipeline operators</span></span>

<span data-ttu-id="da824-213">Canalización `|>` operadores deberían ir debajo de las expresiones que operan en.</span><span class="sxs-lookup"><span data-stu-id="da824-213">Pipeline `|>` operators should go underneath the expressions they operate on.</span></span>

```fsharp
// Preferred approach
let methods2 =
    System.AppDomain.CurrentDomain.GetAssemblies()
    |> List.ofArray
    |> List.map (fun assm -> assm.GetTypes())
    |> Array.concat
    |> List.ofArray
    |> List.map (fun t -> t.GetMethods())
    |> Array.concat

// Not OK
let methods2 = System.AppDomain.CurrentDomain.GetAssemblies()
            |> List.ofArray
            |> List.map (fun assm -> assm.GetTypes())
            |> Array.concat
            |> List.ofArray
            |> List.map (fun t -> t.GetMethods())
            |> Array.concat
```

### <a name="formatting-modules"></a><span data-ttu-id="da824-214">Aplicar formato a los módulos</span><span class="sxs-lookup"><span data-stu-id="da824-214">Formatting modules</span></span>

<span data-ttu-id="da824-215">Código en un módulo local se debe aplicar la sangría en relación con el módulo, pero no debe aplicarse sangría a código en un módulo de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="da824-215">Code in a local module must be indented relative to the module, but code in a top-level module should not be indented.</span></span> <span data-ttu-id="da824-216">Elementos de Namespace no es necesario que tenga la sangría.</span><span class="sxs-lookup"><span data-stu-id="da824-216">Namespace elements do not have to be indented.</span></span>

```fsharp
// A is a top-level module.
module A

let function1 a b = a - b * b
```

```fsharp
// A1 and A2 are local modules.
module A1 =
    let function1 a b = a*a + b*b

module A2 =
    let function2 a b = a*a - b*b
```

### <a name="formatting-object-expressions-and-interfaces"></a><span data-ttu-id="da824-217">Aplicar formato a expresiones de objeto e interfaces</span><span class="sxs-lookup"><span data-stu-id="da824-217">Formatting object expressions and interfaces</span></span>

<span data-ttu-id="da824-218">Expresiones de objeto y las interfaces se deben alinear en la misma manera con `member` que se aplica una sangría después de 4 espacios.</span><span class="sxs-lookup"><span data-stu-id="da824-218">Object expressions and interfaces should be aligned in the same way with `member` being indented after 4 spaces.</span></span>

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-whitespace-in-expressions"></a><span data-ttu-id="da824-219">Espacio en blanco en las expresiones de formato</span><span class="sxs-lookup"><span data-stu-id="da824-219">Formatting whitespace in expressions</span></span>

<span data-ttu-id="da824-220">Evite el espacio en blanco extraño en expresiones de F #.</span><span class="sxs-lookup"><span data-stu-id="da824-220">Avoid extraneous whitespace in F# expressions.</span></span>

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

<span data-ttu-id="da824-221">Argumentos con nombre también no deben tener espacio que rodea el `=`:</span><span class="sxs-lookup"><span data-stu-id="da824-221">Named arguments should also not have space surrounding the `=`:</span></span>

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```