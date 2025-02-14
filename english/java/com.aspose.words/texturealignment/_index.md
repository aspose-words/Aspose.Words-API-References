---
title: TextureAlignment
linktitle: TextureAlignment
second_title: Aspose.Words for Java
description: Specifies the alignment for the tiling of the texture fill in Java.
type: docs
weight: 657
url: /java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

Specifies the alignment for the tiling of the texture fill.

 **Examples:** 

Shows how to fill and tiling the texture inside the shape.

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
## Fields

| Field | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Bottom texture alignment. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | Bottom left texture alignment. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | Bottom right texture alignment. |
| [CENTER](#CENTER) | Center texture alignment. |
| [LEFT](#LEFT) | Left texture alignment. |
| [NONE](#NONE) | None texture alignment. |
| [RIGHT](#RIGHT) | Right texture alignment. |
| [TOP](#TOP) | Top texture alignment. |
| [TOP_LEFT](#TOP-LEFT) | Top left texture alignment. |
| [TOP_RIGHT](#TOP-RIGHT) | Top right texture alignment. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Bottom texture alignment.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


Bottom left texture alignment.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


Bottom right texture alignment.

### CENTER {#CENTER}
```
public static int CENTER
```


Center texture alignment.

### LEFT {#LEFT}
```
public static int LEFT
```


Left texture alignment.

### NONE {#NONE}
```
public static int NONE
```


None texture alignment.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Right texture alignment.

### TOP {#TOP}
```
public static int TOP
```


Top texture alignment.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


Top left texture alignment.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Top right texture alignment.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
