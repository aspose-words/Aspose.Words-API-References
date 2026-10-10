---
title: "TextureAlignment"
linktitle: "TextureAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'alignement du carrelage du remplissage de texture en Java."
type: docs
weight: 680
url: /fr/java/com.aspose.words/texturealignment/
---

**Inheritance:**
java.lang.Object
```
public class TextureAlignment
```

Spécifie l’alignement du carrelage du remplissage de texture.

 **Examples:** 

Montre comment remplir et carreliser la texture à l'intérieur de la forme.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Alignement de texture en bas. |
| [BOTTOM_LEFT](#BOTTOM-LEFT) | Alignement de texture en bas à gauche. |
| [BOTTOM_RIGHT](#BOTTOM-RIGHT) | Alignement de texture en bas à droite. |
| [CENTER](#CENTER) | Alignement de texture au centre. |
| [LEFT](#LEFT) | Alignement de texture à gauche. |
| [NONE](#NONE) | Aucun alignement de texture. |
| [RIGHT](#RIGHT) | Alignement de texture à droite. |
| [TOP](#TOP) | Alignement de texture en haut. |
| [TOP_LEFT](#TOP-LEFT) | Alignement de texture en haut à gauche. |
| [TOP_RIGHT](#TOP-RIGHT) | Alignement de texture en haut à droite. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String textureAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textureAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textureAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Alignement de texture en bas.

### BOTTOM_LEFT {#BOTTOM-LEFT}
```
public static int BOTTOM_LEFT
```


Alignement de texture en bas à gauche.

### BOTTOM_RIGHT {#BOTTOM-RIGHT}
```
public static int BOTTOM_RIGHT
```


Alignement de texture en bas à droite.

### CENTER {#CENTER}
```
public static int CENTER
```


Alignement de texture au centre.

### LEFT {#LEFT}
```
public static int LEFT
```


Alignement de texture à gauche.

### NONE {#NONE}
```
public static int NONE
```


Aucun alignement de texture.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Alignement de texture à droite.

### TOP {#TOP}
```
public static int TOP
```


Alignement de texture en haut.

### TOP_LEFT {#TOP-LEFT}
```
public static int TOP_LEFT
```


Alignement de texture en haut à gauche.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Alignement de texture en haut à droite.

### length {#length}
```
public static int length
```


### fromName(String textureAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textureAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| textureAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textureAlignment) {#getName-int}
```
public static String getName(int textureAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| textureAlignment | int |  |

**Returns:**
java.lang.String
