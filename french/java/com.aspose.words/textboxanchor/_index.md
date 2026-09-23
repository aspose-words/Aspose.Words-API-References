---
title: "TextBoxAnchor"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words pour Java"
description: "Spécifie les valeurs utilisées pour l'alignement vertical du texte de forme en Java."
type: docs
weight: 667
url: /fr/java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

Spécifie les valeurs utilisées pour l'alignement vertical du texte de forme.

 **Examples:** 

Montre comment aligner verticalement le texte d'une zone de texte.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Le texte est aligné en bas de la zone de texte. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | Le texte est aligné sur la ligne de base inférieure de la zone de texte. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | Le texte est aligné au centre inférieur de la zone de texte. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | Le texte est aligné au centre de la ligne de base inférieure de la zone de texte. |
| [MIDDLE](#MIDDLE) | Le texte est aligné au milieu de la zone de texte. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | Le texte est aligné au centre du milieu de la zone de texte. |
| [TOP](#TOP) | Le texte est aligné en haut de la zone de texte. |
| [TOP_BASELINE](#TOP-BASELINE) | Le texte est aligné sur la ligne de base supérieure de la zone de texte. |
| [TOP_CENTERED](#TOP-CENTERED) | Le texte est aligné au centre supérieur de la zone de texte. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | Le texte est aligné au centre de la ligne de base supérieure de la zone de texte. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Le texte est aligné en bas de la zone de texte.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


Le texte est aligné sur la ligne de base inférieure de la zone de texte.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


Le texte est aligné au centre inférieur de la zone de texte.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


Le texte est aligné au centre de la ligne de base inférieure de la zone de texte.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


Le texte est aligné au milieu de la zone de texte.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


Le texte est aligné au centre du milieu de la zone de texte.

### TOP {#TOP}
```
public static int TOP
```


Le texte est aligné en haut de la zone de texte.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


Le texte est aligné sur la ligne de base supérieure de la zone de texte.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


Le texte est aligné au centre supérieur de la zone de texte.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


Le texte est aligné au centre de la ligne de base supérieure de la zone de texte.

### length {#length}
```
public static int length
```


### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
