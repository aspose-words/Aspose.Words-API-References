---
title: "TextureAlignment"
linktitle: "TextureAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento per la ripetizione del riempimento texture in Java."
type: docs
weight: 680
url: /it/java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

Specifica l'allineamento per la piastrellatura del riempimento texture.

 **Examples:** 

Mostra come riempire e ripetere la texture all'interno della forma.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTTOM](#BOTTOM) | Allineamento texture inferiore. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | Allineamento texture inferiore sinistro. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | Allineamento texture inferiore destro. |
| [CENTER](#CENTER) | Allineamento texture centrale. |
| [LEFT](#LEFT) | Allineamento texture sinistro. |
| [NONE](#NONE) | Nessun allineamento texture. |
| [RIGHT](#RIGHT) | Allineamento texture destro. |
| [TOP](#TOP) | Allineamento texture superiore. |
| [TOP_LEFT](#TOP-LEFT) | Allineamento texture superiore sinistro. |
| [TOP_RIGHT](#TOP-RIGHT) | Allineamento texture superiore destro. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Allineamento texture inferiore.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


Allineamento texture inferiore sinistro.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


Allineamento texture inferiore destro.

### CENTER {#CENTER}
```
public static int CENTER
```


Allineamento texture centrale.

### LEFT {#LEFT}
```
public static int LEFT
```


Allineamento texture sinistro.

### NONE {#NONE}
```
public static int NONE
```


Nessun allineamento texture.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Allineamento texture destro.

### TOP {#TOP}
```
public static int TOP
```


Allineamento texture superiore.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


Allineamento texture superiore sinistro.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Allineamento texture superiore destro.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
