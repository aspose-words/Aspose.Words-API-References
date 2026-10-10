---
title: "TextureAlignment"
linktitle: "TextureAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la alineación para el mosaico del relleno de textura en Java."
type: docs
weight: 680
url: /es/java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

Especifica la alineación para el mosaico del relleno de textura.

 **Examples:** 

Muestra cómo rellenar y mosaicar la textura dentro de la forma.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTTOM](#BOTTOM) | Alineación de textura inferior. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | Alineación de textura inferior izquierda. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | Alineación de textura inferior derecha. |
| [CENTER](#CENTER) | Alineación de textura centrada. |
| [LEFT](#LEFT) | Alineación de textura izquierda. |
| [NONE](#NONE) | Sin alineación de textura. |
| [RIGHT](#RIGHT) | Alineación de textura derecha. |
| [TOP](#TOP) | Alineación de textura superior. |
| [TOP_LEFT](#TOP-LEFT) | Alineación de textura superior izquierda. |
| [TOP_RIGHT](#TOP-RIGHT) | Alineación de textura superior derecha. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Alineación de textura inferior.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


Alineación de textura inferior izquierda.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


Alineación de textura inferior derecha.

### CENTER {#CENTER}
```
public static int CENTER
```


Alineación de textura centrada.

### LEFT {#LEFT}
```
public static int LEFT
```


Alineación de textura izquierda.

### NONE {#NONE}
```
public static int NONE
```


Sin alineación de textura.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Alineación de textura derecha.

### TOP {#TOP}
```
public static int TOP
```


Alineación de textura superior.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


Alineación de textura superior izquierda.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Alineación de textura superior derecha.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
