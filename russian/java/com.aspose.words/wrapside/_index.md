---
title: "WrapSide"
linktitle: "WrapSide"
second_title: "Aspose.Words для Java"
description: "Указывает, какие стороны фигуры или изображения обтекает текст в Java."
type: docs
weight: 736
url: /ru/java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

Указывает, с какой стороны(сторон) формы или изображения обтекает текст.

 **Examples:** 

Показывает, как заменить все формы текстовых полей на формы изображений.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BOTH](#BOTH) | Текст документа обтекает фигуру с обеих сторон. |
| [DEFAULT](#DEFAULT) | Значение по умолчанию — [BOTH](../../com.aspose.words/wrapside/\#BOTH). |
| [LARGEST](#LARGEST) | Текст документа обтекает фигуру со стороны, наиболее удалённой от полей страницы, оставляя свободную область текста с другой стороны фигуры. |
| [LEFT](#LEFT) | Текст документа обтекает фигуру только с левой стороны. |
| [RIGHT](#RIGHT) | Текст документа обтекает фигуру только с правой стороны. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapSide)](#toString-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


Текст документа обтекает фигуру с обеих сторон.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию — [BOTH](../../com.aspose.words/wrapside/\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


Текст документа обтекает фигуру со стороны, наиболее удалённой от полей страницы, оставляя свободную область текста с другой стороны фигуры.

### LEFT {#LEFT}
```
public static int LEFT
```


Текст документа обтекает фигуру только с левой стороны. С правой стороны фигуры остаётся свободная область текста.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Текст документа обтекает фигуру только с правой стороны. С левой стороны фигуры остаётся свободная область текста.

### length {#length}
```
public static int length
```


### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
