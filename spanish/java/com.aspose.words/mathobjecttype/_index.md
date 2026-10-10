---
title: "MathObjectType"
linktitle: "MathObjectType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de un objeto Office Math en Java."
type: docs
weight: 459
url: /es/java/com.aspose.words/mathobjecttype/
---

**Inheritance:**
java.lang.Object
```
public class MathObjectType
```

Especifica el tipo de un objeto Office Math.

 **Examples:** 

Muestra cómo imprimir la estructura de nodos de cada nodo de Office Math en un documento.

```

 public void officeMathToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered OfficeMath nodes and their children.
 /// 
 public static class OfficeMathStructurePrinter extends DocumentVisitor {
     public OfficeMathStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideOfficeMath = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideOfficeMath) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an OfficeMath node is encountered in the document.
     /// 
     public int visitOfficeMathStart(final OfficeMath officeMath) {
         indentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.getMathObjectType());
         mDocTraversalDepth++;
         mVisitorIsInsideOfficeMath = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of an OfficeMath node have been visited.
     /// 
     public int visitOfficeMathEnd(final OfficeMath officeMath) {
         mDocTraversalDepth--;
         indentAndAppendLine("[OfficeMath end]");
         mVisitorIsInsideOfficeMath = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideOfficeMath;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ACCENT](#ACCENT) | Función de acento, que consiste en una base y una marca diacrítica combinada. |
| [ARGUMENT](#ARGUMENT) | Objeto de argumento. |
| [ARRAY](#ARRAY) | Objeto de matriz, que consiste en una o más ecuaciones, expresiones u otras secuencias de texto matemático que pueden justificarse verticalmente como una unidad con respecto al texto circundante en la línea. |
| [BAR](#BAR) | Función de barra, que consiste en un argumento base y una barra superior o inferior. |
| [BORDER_BOX](#BORDER-BOX) | Objeto Border Box, que consiste en un borde dibujado alrededor de una instancia de texto matemático (como una fórmula o ecuación). |
| [BOX](#BOX) | Objeto Box, que se utiliza para agrupar componentes de una ecuación u otra instancia de texto matemático. |
| [DEGREE](#DEGREE) | Grado en el radical matemático. |
| [DELIMITER](#DELIMITER) | Objeto delimitador, que consiste en delimitadores de apertura y cierre (como paréntesis, llaves, corchetes y barras verticales), y un elemento contenido dentro. |
| [DENOMINATOR](#DENOMINATOR) | Denominador de un objeto fracción. |
| [FRACTION](#FRACTION) | Objeto fracción, que consiste en un numerador y un denominador separados por una barra de fracción. |
| [FUNCTION](#FUNCTION) | Objeto Function-Apply, que consiste en un nombre de función y un elemento de argumento al que se aplica. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Nombre de la función. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Objeto Group-Character, que consiste en un carácter dibujado encima o debajo del texto, a menudo con el propósito de agrupar visualmente los elementos. |
| [LIMIT](#LIMIT) | Límite inferior del objeto [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/#LOWER-LIMIT) y límite superior de la función [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/#UPPER-LIMIT). |
| [LOWER_LIMIT](#LOWER-LIMIT) | Objeto Lower-Limit, que consiste en texto en la línea base y texto de tamaño reducido inmediatamente debajo de él. |
| [MATRIX](#MATRIX) | Objeto matriz, que consiste en uno o más elementos dispuestos en una o más filas y una o más columnas. |
| [MATRIX_ROW](#MATRIX-ROW) | Fila única de la matriz. |
| [NONE](#NONE) | El tipo de objeto no está especificado. |
| [NUMERATOR](#NUMERATOR) | Numerador del objeto Fracción. |
| [N_ARY](#N-ARY) | Objeto N-ary, que consiste en un objeto n-ario, una base (u operando) y límites superior e inferior opcionales. |
| [O_MATH](#O-MATH) | Instancia de texto matemático. |
| [O_MATH_PARA](#O-MATH-PARA) | Párrafo matemático, o zona de visualización de matemáticas, que contiene uno o más elementos [O\_MATH](../../com.aspose.words/mathobjecttype/#O-MATH) que están en modo de visualización. |
| [PHANTOM](#PHANTOM) | Objeto fantasma. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Objeto Pre-Sub-Superscript, que consiste en un elemento base y un subíndice y superíndice colocados a la izquierda de la base. |
| [RADICAL](#RADICAL) | Objeto radical, que consiste en un radical, un elemento base y un grado opcional. |
| [SUBSCRIPT](#SUBSCRIPT) | Objeto subíndice, que consiste en un elemento base y un script de tamaño reducido colocado debajo y a la derecha. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Subíndice del objeto que puede tener una parte subíndice. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Objeto sub-superscript, que consiste en un elemento base, un script de tamaño reducido colocado debajo y a la derecha, y un script de tamaño reducido colocado encima y a la derecha. |
| [SUPERSCRIPT](#SUPERSCRIPT) | Objeto superscript, que consiste en un elemento base y un script de tamaño reducido colocado encima y a la derecha. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Superscript del objeto superscript. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Objeto límite superior, que consiste en texto en la línea base y texto de tamaño reducido inmediatamente encima de él. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String) |  |
| [getName(int mathObjectType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mathObjectType)](#toString-int) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Función de acento, que consiste en una base y una marca diacrítica combinada.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Objeto argumento. Encierra entidades de Office Math cuando se usan como argumentos de otras entidades de Office Math.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Objeto de matriz, que consiste en una o más ecuaciones, expresiones u otras secuencias de texto matemático que pueden justificarse verticalmente como una unidad con respecto al texto circundante en la línea.

### BAR {#BAR}
```
public static int BAR
```


Función de barra, que consiste en un argumento base y una barra superior o inferior.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Objeto Border Box, que consiste en un borde dibujado alrededor de una instancia de texto matemático (como una fórmula o ecuación).

### BOX {#BOX}
```
public static int BOX
```


Objeto Box, que se utiliza para agrupar componentes de una ecuación u otra instancia de texto matemático.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Grado en el radical matemático.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Objeto delimitador, que consiste en delimitadores de apertura y cierre (como paréntesis, llaves, corchetes y barras verticales), y un elemento contenido dentro.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Denominador de un objeto fracción.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Objeto fracción, que consiste en un numerador y un denominador separados por una barra de fracción.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Objeto Function-Apply, que consiste en un nombre de función y un elemento de argumento al que se aplica.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Nombre de la función. Por ejemplo, los nombres de funciones son sin y cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Objeto Group-Character, que consiste en un carácter dibujado encima o debajo del texto, a menudo con el propósito de agrupar visualmente los elementos.

### LIMIT {#LIMIT}
```
public static int LIMIT
```


Límite inferior del objeto [LOWER\_LIMIT](../../com.aspose.words/mathobjecttype/#LOWER-LIMIT) y límite superior de la función [UPPER\_LIMIT](../../com.aspose.words/mathobjecttype/#UPPER-LIMIT).

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Objeto Lower-Limit, que consiste en texto en la línea base y texto de tamaño reducido inmediatamente debajo de él.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Objeto matriz, que consiste en uno o más elementos dispuestos en una o más filas y una o más columnas.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Fila única de la matriz.

### NONE {#NONE}
```
public static int NONE
```


El tipo de objeto no está especificado.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Numerador del objeto Fracción.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


Objeto N-ary, que consiste en un objeto n-ario, una base (u operando) y límites superior e inferior opcionales.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Instancia de texto matemático.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


Párrafo matemático, o zona de visualización de matemáticas, que contiene uno o más elementos [O\_MATH](../../com.aspose.words/mathobjecttype/#O-MATH) que están en modo de visualización.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Objeto fantasma.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Objeto Pre-Sub-Superscript, que consiste en un elemento base y un subíndice y superíndice colocados a la izquierda de la base.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Objeto radical, que consiste en un radical, un elemento base y un grado opcional.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Objeto subíndice, que consiste en un elemento base y un script de tamaño reducido colocado debajo y a la derecha.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Subíndice del objeto que puede tener una parte subíndice.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Objeto sub-superscript, que consiste en un elemento base, un script de tamaño reducido colocado debajo y a la derecha, y un script de tamaño reducido colocado encima y a la derecha.

### SUPERSCRIPT {#SUPERSCRIPT}
```
public static int SUPERSCRIPT
```


Objeto superscript, que consiste en un elemento base y un script de tamaño reducido colocado encima y a la derecha.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Superscript del objeto superscript.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Objeto límite superior, que consiste en texto en la línea base y texto de tamaño reducido inmediatamente encima de él.

### length {#length}
```
public static int length
```


### fromName(String mathObjectTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mathObjectTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mathObjectType) {#getName-int}
```
public static String getName(int mathObjectType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mathObjectType) {#toString-int}
```
public static String toString(int mathObjectType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mathObjectType | int |  |

**Returns:**
java.lang.String
