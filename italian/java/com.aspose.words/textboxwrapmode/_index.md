---
title: "TextBoxWrapMode"
linktitle: "TextBoxWrapMode"
second_title: "Aspose.Words per Java"
description: "Specifica come il testo viene avvolto all'interno di una forma in Java."
type: docs
weight: 669
url: /it/java/com.aspose.words/textboxwrapmode/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxWrapMode
```

Specifica come il testo si avvolge all'interno di una forma.

 **Examples:** 

Mostra come impostare una modalità di avvolgimento per il contenuto di una casella di testo.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [NONE](#NONE) | Il testo non viene avvolto all'interno di una forma. |
| [SQUARE](#SQUARE) | Il testo viene avvolto all'interno di una forma. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String textBoxWrapModeName)](#fromName-java.lang.String) |  |
| [getName(int textBoxWrapMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxWrapMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Il testo non viene avvolto all'interno di una forma.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Il testo viene avvolto all'interno di una forma.

### length {#length}
```
public static int length
```


### fromName(String textBoxWrapModeName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxWrapModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textBoxWrapModeName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxWrapMode) {#getName-int}
```
public static String getName(int textBoxWrapMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textBoxWrapMode | int |  |

**Returns:**
java.lang.String
