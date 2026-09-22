---
title: "WrapSide"
linktitle: "WrapSide"
second_title: "Aspose.Words لـ Java"
description: "يحدد أي جوانب الشكل أو الصورة يلتف حولها النص في جافا."
type: docs
weight: 736
url: /ar/java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

يحدد الجوانب التي يلتف حولها النص بالنسبة للشكل أو الصورة.

 **Examples:** 

يوضح كيفية استبدال جميع أشكال مربعات النص بأشكال الصور.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTH](#BOTH) | النص في المستند يلتف على جانبي الشكل. |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية هي [BOTH](../../com.aspose.words/wrapside/\#BOTH). |
| [LARGEST](#LARGEST) | النص في المستند يلتف على الجانب من الشكل الأبعد عن هامش الصفحة، مما يترك مساحة خالية للنص على الجانب الآخر من الشكل. |
| [LEFT](#LEFT) | النص في المستند يلتف على الجانب الأيسر من الشكل فقط. |
| [RIGHT](#RIGHT) | النص في المستند يلتف على الجانب الأيمن من الشكل فقط. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapSide)](#toString-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


النص في المستند يلتف على جانبي الشكل.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية هي [BOTH](../../com.aspose.words/wrapside/\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


النص في المستند يلتف على الجانب من الشكل الأبعد عن هامش الصفحة، مما يترك مساحة خالية للنص على الجانب الآخر من الشكل.

### LEFT {#LEFT}
```
public static int LEFT
```


النص في المستند يلتف على الجانب الأيسر من الشكل فقط. هناك مساحة خالية للنص على يمين الشكل.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


النص في المستند يلتف على الجانب الأيمن من الشكل فقط. هناك مساحة خالية للنص على يسار الشكل.

### length {#length}
```
public static int length
```


### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
