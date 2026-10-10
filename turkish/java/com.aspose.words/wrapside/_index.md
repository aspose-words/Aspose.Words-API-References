---
title: "WrapSide"
linktitle: "WrapSide"
second_title: "Aspose.Words Java için"
description: "Java'da metnin şekil veya resmin hangi taraflarına dolandığını belirtir."
type: docs
weight: 736
url: /tr/java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

Metnin şekil veya resmin hangi taraf(lar)ı etrafında dolandığını belirtir.

 **Examples:** 

Tüm metin kutusu şekillerinin nasıl görüntü şekilleriyle değiştirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOTH](#BOTH) | Belge metni şeklin her iki tarafına da dolanır. |
| [DEFAULT](#DEFAULT) | Varsayılan değer [BOTH](../../com.aspose.words/wrapside/\\#BOTH) dir. |
| [LARGEST](#LARGEST) | Belge metni, sayfa kenar boşluğundan en uzak olan şekil tarafına dolanır ve şeklin diğer tarafında metin boş alanı bırakır. |
| [LEFT](#LEFT) | Belge metni yalnızca şeklin sol tarafına dolanır. |
| [RIGHT](#RIGHT) | Belge metni yalnızca şeklin sağ tarafına dolanır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapSide)](#toString-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


Belge metni şeklin her iki tarafına da dolanır.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer [BOTH](../../com.aspose.words/wrapside/\\#BOTH) dir.

### LARGEST {#LARGEST}
```
public static int LARGEST
```


Belge metni, sayfa kenar boşluğundan en uzak olan şekil tarafına dolanır ve şeklin diğer tarafında metin boş alanı bırakır.

### LEFT {#LEFT}
```
public static int LEFT
```


Belge metni yalnızca şeklin sol tarafına dolanır. Şeklin sağ tarafında metin boş alanı vardır.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Belge metni yalnızca şeklin sağ tarafına dolanır. Şeklin sol tarafında metin boş alanı vardır.

### length {#length}
```
public static int length
```


### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int wrapSide) {#toString-int}
```
public static String toString(int wrapSide)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
