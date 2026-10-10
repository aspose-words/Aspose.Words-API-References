---
title: "TextBoxWrapMode"
linktitle: "TextBoxWrapMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se ajusta el texto dentro de una forma en Java."
type: docs
weight: 669
url: /es/java/com.aspose.words/textboxwrapmode/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxWrapMode
```

Especifica cómo se ajusta el texto dentro de una forma.

 **Examples:** 

Muestra cómo establecer un modo de ajuste para el contenido de un cuadro de texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 300.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.None" to increase the text box's width
 // to accommodate text, should it be large enough.
 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.Square" to
 // wrap all text inside the text box, preserving its dimensions.
 textBox.setTextBoxWrapMode(textBoxWrapMode);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.getFont().setSize(32.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "Shape.TextBoxContentsWrapMode.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [NONE](#NONE) | El texto no se ajusta dentro de una forma. |
| [SQUARE](#SQUARE) | El texto se ajusta dentro de una forma. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String textBoxWrapModeName)](#fromName-java.lang.String) |  |
| [getName(int textBoxWrapMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxWrapMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


El texto no se ajusta dentro de una forma.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


El texto se ajusta dentro de una forma.

### length {#length}
```
public static int length
```


### fromName(String textBoxWrapModeName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxWrapModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textBoxWrapModeName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxWrapMode) {#getName-int}
```
public static String getName(int textBoxWrapMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textBoxWrapMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textBoxWrapMode) {#toString-int}
```
public static String toString(int textBoxWrapMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textBoxWrapMode | int |  |

**Returns:**
java.lang.String
