---
title: "Enumeración Aspose::Words::Math::MathObjectType"
linktitle: "MathObjectType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Math::MathObjectType. Especifica el tipo de un objeto Office Math en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Especifica el tipo de un objeto Office [Math](../).

```cpp
enum class MathObjectType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| OMath | 0 | Instancia de texto matemático. |
| OMathPara | 1 | Párrafo [Math](../), o zona de matemáticas de visualización, que contiene uno o más elementos [OMath](./) que están en modo de visualización. |
| Accent | 2 | Función Accent, que consiste en una base y una marca diacrítica combinada. |
| Bar | 3 | Función Bar, que consiste en un argumento base y una barra superior o inferior. |
| BorderBox | 4 | [Border](../../aspose.words/border/) Objeto Box, que consiste en un borde dibujado alrededor de una instancia de texto matemático (como una fórmula o ecuación). |
| Box | 5 | Objeto Box, que se usa para agrupar componentes de una ecuación u otra instancia de texto matemático. |
| Delimitador | 6 | Objeto delimitador, que consiste en delimitadores de apertura y cierre (como paréntesis, llaves, corchetes y barras verticales), y un elemento contenido dentro. |
| Grado | 7 | Grado en el radical matemático. |
| Argument | 8 | Objeto argumento. Encierra entidades de Office [Math](../) cuando se utilizan como argumentos de otras entidades de Office [Math](../). |
| Arreglo | 9 | Objeto arreglo, que consiste en una o más ecuaciones, expresiones u otras secuencias de texto matemático que pueden justificarse verticalmente como una unidad respecto al texto circundante en la línea. |
| Fracción | 10 | Objeto fracción, que consiste en un numerador y un denominador separados por una barra de fracción. |
| Denominador | 11 | Denominador de un objeto fracción. |
| Numerador | 12 | Numerador del objeto Fracción. |
| Función | 13 | Objeto Función-Aplicar, que consiste en un nombre de función y un elemento argumento sobre el cual se actúa. |
| FunctionName | 14 | Nombre de la función. Por ejemplo, los nombres de funciones son sin y cos. |
| GroupCharacter | 15 | Objeto Grupo-Caracter, que consiste en un carácter dibujado encima o debajo del texto, a menudo con el propósito de agrupar visualmente los elementos. |
| Limit | 16 | Límite inferior del objeto [LowerLimit](./) y el límite superior de la función [UpperLimit](./). |
| LowerLimit | 17 | Objeto Límite-Inferior, que consiste en texto en la línea base y texto de tamaño reducido inmediatamente debajo de él. |
| UpperLimit | 18 | Objeto Límite-Superior, que consiste en texto en la línea base y texto de tamaño reducido inmediatamente encima de él. |
| Matriz | 19 | Objeto matriz, que consiste en uno o más elementos dispuestos en una o más filas y una o más columnas. |
| MatrixRow | 20 | Fila única de la matriz. |
| NAry | 21 | Objeto n-ario, que consiste en un objeto n-ario, una base (u operando) y límites superior e inferior opcionales. |
| Phantom | 22 | Objeto fantasma. |
| Radical | 23 | Objeto radical, que consiste en un radical, un elemento base y un grado opcional. |
| SubscriptPart | 24 | Subíndice del objeto que puede tener parte de subíndice. |
| SuperscriptPart | 25 | Superíndice del objeto superíndice. |
| PreSubSuperscript | 26 | Objeto Pre-Sub-Superíndice, que consiste en un elemento base y un subíndice y superíndice colocados a la izquierda de la base. |
| Subscript | 27 | Objeto subíndice, que consiste en un elemento base y un script de tamaño reducido colocado debajo y a la derecha. |
| SubSuperscript | 28 | Objeto sub-superíndice, que consiste en un elemento base, un script de tamaño reducido colocado debajo y a la derecha, y un script de tamaño reducido colocado encima y a la derecha. |
| Superscript | 29 | Objeto superíndice, que consiste en un elemento base y un script de tamaño reducido colocado encima y a la derecha. |
| None | 30 | Tipo de objeto no especificado. |

## Ver también

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
