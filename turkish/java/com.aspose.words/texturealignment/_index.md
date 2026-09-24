---
title: "TextureAlignment"
linktitle: "TextureAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da doku doldurmanın döşenmesi için hizalamayı belirtir."
type: docs
weight: 680
url: /tr/java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

Doku doldurmanın döşenmesi için hizalamayı belirtir.

 **Examples:** 

Şekil içinde dokuyu doldurma ve döşeme yöntemini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOTTOM](#BOTTOM) | Alt doku hizalaması. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | Alt sol doku hizalaması. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | Alt sağ doku hizalaması. |
| [CENTER](#CENTER) | Orta doku hizalaması. |
| [LEFT](#LEFT) | Sol doku hizalaması. |
| [NONE](#NONE) | Hiç doku hizalaması. |
| [RIGHT](#RIGHT) | Sağ doku hizalaması. |
| [TOP](#TOP) | Üst doku hizalaması. |
| [TOP_LEFT](#TOP-LEFT) | Üst sol doku hizalaması. |
| [TOP_RIGHT](#TOP-RIGHT) | Üst sağ doku hizalaması. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Alt doku hizalaması.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


Alt sol doku hizalaması.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


Alt sağ doku hizalaması.

### CENTER {#CENTER}
```
public static int CENTER
```


Orta doku hizalaması.

### LEFT {#LEFT}
```
public static int LEFT
```


Sol doku hizalaması.

### NONE {#NONE}
```
public static int NONE
```


Hiç doku hizalaması.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Sağ doku hizalaması.

### TOP {#TOP}
```
public static int TOP
```


Üst doku hizalaması.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


Üst sol doku hizalaması.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Üst sağ doku hizalaması.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
