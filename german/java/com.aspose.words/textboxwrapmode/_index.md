---
title: "TextBoxWrapMode"
linktitle: "TextBoxWrapMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Text innerhalb einer Form in Java umbrochen wird."
type: docs
weight: 669
url: /de/java/com.aspose.words/textboxwrapmode/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxWrapMode
```

Gibt an, wie Text innerhalb einer Form umbrochen wird.

 **Examples:** 

Zeigt, wie ein Umbruchmodus für den Inhalt einer Textbox festgelegt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [NONE](#NONE) | Text wird innerhalb einer Form nicht umbrochen. |
| [SQUARE](#SQUARE) | Text wird innerhalb einer Form umbrochen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String textBoxWrapModeName)](#fromName-java.lang.String) |  |
| [getName(int textBoxWrapMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxWrapMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Text wird innerhalb einer Form nicht umbrochen.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Text wird innerhalb einer Form umbrochen.

### length {#length}
```
public static int length
```


### fromName(String textBoxWrapModeName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxWrapModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textBoxWrapModeName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxWrapMode) {#getName-int}
```
public static String getName(int textBoxWrapMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textBoxWrapMode | int |  |

**Returns:**
java.lang.String
