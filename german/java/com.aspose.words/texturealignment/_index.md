---
title: "TextureAlignment"
linktitle: "TextureAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die Ausrichtung für die Kachelung der Texturfüllung in Java an."
type: docs
weight: 680
url: /de/java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

Gibt die Ausrichtung für das Kacheln der Texturfüllung an.

 **Examples:** 

Zeigt, wie die Textur innerhalb der Form gefüllt und gekachelt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);

 // Apply texture alignment to the shape fill.
 shape.getFill().presetTextured(PresetTexture.CANVAS);
 shape.getFill().setTextureAlignment(TextureAlignment.TOP_RIGHT);

 // Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
 // property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.TextureFill.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "Shape.TextureFill.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals(TextureAlignment.TOP_RIGHT, shape.getFill().getTextureAlignment());
 Assert.assertEquals(PresetTexture.CANVAS, shape.getFill().getPresetTexture());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOTTOM](#BOTTOM) | Untere Texturausrichtung. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | Untere linke Texturausrichtung. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | Untere rechte Texturausrichtung. |
| [CENTER](#CENTER) | Zentrierte Texturausrichtung. |
| [LEFT](#LEFT) | Linke Texturausrichtung. |
| [NONE](#NONE) | Keine Texturausrichtung. |
| [RIGHT](#RIGHT) | Rechte Texturausrichtung. |
| [TOP](#TOP) | Obere Texturausrichtung. |
| [TOP_LEFT](#TOP-LEFT) | Obere linke Texturausrichtung. |
| [TOP_RIGHT](#TOP-RIGHT) | Obere rechte Texturausrichtung. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Untere Texturausrichtung.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


Untere linke Texturausrichtung.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


Untere rechte Texturausrichtung.

### CENTER {#CENTER}
```
public static int CENTER
```


Zentrierte Texturausrichtung.

### LEFT {#LEFT}
```
public static int LEFT
```


Linke Texturausrichtung.

### NONE {#NONE}
```
public static int NONE
```


Keine Texturausrichtung.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Rechte Texturausrichtung.

### TOP {#TOP}
```
public static int TOP
```


Obere Texturausrichtung.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


Obere linke Texturausrichtung.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Obere rechte Texturausrichtung.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textureAlignment) {#toString-int}
```
public static String toString(int textureAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
