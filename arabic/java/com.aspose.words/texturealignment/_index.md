---
title: "TextureAlignment"
linktitle: "TextureAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد المحاذاة لتكرار تعبئة النسيج في Java."
type: docs
weight: 680
url: /ar/java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

يحدد المحاذاة لتكرار تعبئة النسيج.

 **Examples:** 

يظهر كيفية تعبئة وتكرار النسيج داخل الشكل.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTTOM](#BOTTOM) | محاذاة النسيج السفلية. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | محاذاة النسيج السفلية اليسرى. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | محاذاة النسيج السفلية اليمنى. |
| [CENTER](#CENTER) | محاذاة النسيج المركزية. |
| [LEFT](#LEFT) | محاذاة النسيج اليسرى. |
| [NONE](#NONE) | لا محاذاة للنسيج. |
| [RIGHT](#RIGHT) | محاذاة النسيج اليمنى. |
| [TOP](#TOP) | محاذاة النسيج العلوية. |
| [TOP_LEFT](#TOP-LEFT) | محاذاة النسيج العلوية اليسرى. |
| [TOP_RIGHT](#TOP-RIGHT) | محاذاة النسيج العلوية اليمنى. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


محاذاة النسيج السفلية.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


محاذاة النسيج السفلية اليسرى.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


محاذاة النسيج السفلية اليمنى.

### CENTER {#CENTER}
```
public static int CENTER
```


محاذاة النسيج المركزية.

### LEFT {#LEFT}
```
public static int LEFT
```


محاذاة النسيج اليسرى.

### NONE {#NONE}
```
public static int NONE
```


لا محاذاة للنسيج.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


محاذاة النسيج اليمنى.

### TOP {#TOP}
```
public static int TOP
```


محاذاة النسيج العلوية.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


محاذاة النسيج العلوية اليسرى.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


محاذاة النسيج العلوية اليمنى.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
