---
title: "TextBoxAnchor"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words para Java"
description: "Especifica los valores utilizados para la alineación vertical del texto de la forma en Java."
type: docs
weight: 667
url: /es/java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

Especifica los valores usados para la alineación vertical del texto de la forma.

 **Examples:** 

Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTTOM](#BOTTOM) | El texto está alineado en la parte inferior del cuadro de texto. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | El texto está alineado en la línea base inferior del cuadro de texto. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | El texto está alineado centrado en la parte inferior del cuadro de texto. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | El texto está alineado centrado en la línea base inferior del cuadro de texto. |
| [MIDDLE](#MIDDLE) | El texto está alineado en el medio del cuadro de texto. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | El texto está alineado centrado en el medio del cuadro de texto. |
| [TOP](#TOP) | El texto está alineado en la parte superior del cuadro de texto. |
| [TOP_BASELINE](#TOP-BASELINE) | El texto está alineado en la línea base superior del cuadro de texto. |
| [TOP_CENTERED](#TOP-CENTERED) | El texto está alineado centrado en la parte superior del cuadro de texto. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | El texto está alineado centrado en la línea base superior del cuadro de texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


El texto está alineado en la parte inferior del cuadro de texto.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


El texto está alineado en la línea base inferior del cuadro de texto.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


El texto está alineado centrado en la parte inferior del cuadro de texto.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


El texto está alineado centrado en la línea base inferior del cuadro de texto.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


El texto está alineado en el medio del cuadro de texto.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


El texto está alineado centrado en el medio del cuadro de texto.

### TOP {#TOP}
```
public static int TOP
```


El texto está alineado en la parte superior del cuadro de texto.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


El texto está alineado en la línea base superior del cuadro de texto.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


El texto está alineado centrado en la parte superior del cuadro de texto.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


El texto está alineado centrado en la línea base superior del cuadro de texto.

### length {#length}
```
public static int length
```


### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textBoxAnchor) {#toString-int}
```
public static String toString(int textBoxAnchor)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
