---
title: "TextBoxAnchor"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words für Java"
description: "Gibt die Werte an, die für die vertikale Ausrichtung von Formtext in Java verwendet werden."
type: docs
weight: 667
url: /de/java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

Gibt Werte für die vertikale Ausrichtung von Formtext an.

 **Examples:** 

Zeigt, wie der Textinhalt einer Textbox vertikal ausgerichtet wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOTTOM](#BOTTOM) | Der Text ist am unteren Rand des Textfelds ausgerichtet. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | Der Text ist an der unteren Grundlinie des Textfelds ausgerichtet. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | Der Text ist unten zentriert im Textfeld ausgerichtet. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | Der Text ist an der unten zentrierten Grundlinie des Textfelds ausgerichtet. |
| [MIDDLE](#MIDDLE) | Der Text ist in der Mitte des Textfelds ausgerichtet. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | Der Text ist mittig zentriert im Textfeld ausgerichtet. |
| [TOP](#TOP) | Der Text ist am oberen Rand des Textfelds ausgerichtet. |
| [TOP_BASELINE](#TOP-BASELINE) | Der Text ist an der oberen Grundlinie des Textfelds ausgerichtet. |
| [TOP_CENTERED](#TOP-CENTERED) | Der Text ist oben zentriert im Textfeld ausgerichtet. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | Der Text ist an der oben zentrierten Grundlinie des Textfelds ausgerichtet. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Der Text ist am unteren Rand des Textfelds ausgerichtet.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


Der Text ist an der unteren Grundlinie des Textfelds ausgerichtet.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


Der Text ist unten zentriert im Textfeld ausgerichtet.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


Der Text ist an der unten zentrierten Grundlinie des Textfelds ausgerichtet.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


Der Text ist in der Mitte des Textfelds ausgerichtet.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


Der Text ist mittig zentriert im Textfeld ausgerichtet.

### TOP {#TOP}
```
public static int TOP
```


Der Text ist am oberen Rand des Textfelds ausgerichtet.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


Der Text ist an der oberen Grundlinie des Textfelds ausgerichtet.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


Der Text ist oben zentriert im Textfeld ausgerichtet.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


Der Text ist an der oben zentrierten Grundlinie des Textfelds ausgerichtet.

### length {#length}
```
public static int length
```


### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
