---
title: "TextureAlignment"
linktitle: "TextureAlignment"
second_title: "Aspose.Words для Java"
description: "Указывает выравнивание для замощения текстурного заполнения в Java."
type: docs
weight: 680
url: /ru/java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

Указывает выравнивание при черепичной заливке текстурой.

 **Examples:** 

Показывает, как заполнять и замощать текстуру внутри фигуры.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BOTTOM](#BOTTOM) | Выравнивание текстуры по нижнему краю. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | Выравнивание текстуры по нижнему левому углу. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | Выравнивание текстуры по нижнему правому углу. |
| [CENTER](#CENTER) | Выравнивание текстуры по центру. |
| [LEFT](#LEFT) | Выравнивание текстуры по левому краю. |
| [NONE](#NONE) | Отсутствие выравнивания текстуры. |
| [RIGHT](#RIGHT) | Выравнивание текстуры по правому краю. |
| [TOP](#TOP) | Выравнивание текстуры по верхнему краю. |
| [TOP_LEFT](#TOP-LEFT) | Выравнивание текстуры по верхнему левому углу. |
| [TOP_RIGHT](#TOP-RIGHT) | Выравнивание текстуры по верхнему правому углу. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Выравнивание текстуры по нижнему краю.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


Выравнивание текстуры по нижнему левому углу.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


Выравнивание текстуры по нижнему правому углу.

### CENTER {#CENTER}
```
public static int CENTER
```


Выравнивание текстуры по центру.

### LEFT {#LEFT}
```
public static int LEFT
```


Выравнивание текстуры по левому краю.

### NONE {#NONE}
```
public static int NONE
```


Отсутствие выравнивания текстуры.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Выравнивание текстуры по правому краю.

### TOP {#TOP}
```
public static int TOP
```


Выравнивание текстуры по верхнему краю.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


Выравнивание текстуры по верхнему левому углу.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Выравнивание текстуры по верхнему правому углу.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
