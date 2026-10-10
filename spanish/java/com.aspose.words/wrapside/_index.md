---
title: "WrapSide"
linktitle: "WrapSide"
second_title: "Aspose.Words para Java"
description: "Especifica en qué lados de la forma o imagen el texto se envuelve en Java."
type: docs
weight: 736
url: /es/java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

Especifica en qué lado(s) de la forma o imagen se envuelve el texto.

 **Examples:** 

Muestra cómo reemplazar todas las formas de cuadro de texto por formas de imagen.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTH](#BOTH) | El texto del documento se envuelve en ambos lados de la forma. |
| [DEFAULT](#DEFAULT) | El valor predeterminado es [BOTH](../../com.aspose.words/wrapside/\#BOTH). |
| [LARGEST](#LARGEST) | El texto del documento se envuelve en el lado de la forma que está más alejado del margen de la página, dejando un área libre de texto en el otro lado de la forma. |
| [LEFT](#LEFT) | El texto del documento se envuelve solo en el lado izquierdo de la forma. |
| [RIGHT](#RIGHT) | El texto del documento se envuelve solo en el lado derecho de la forma. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapSide)](#toString-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


El texto del documento se envuelve en ambos lados de la forma.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


El valor predeterminado es [BOTH](../../com.aspose.words/wrapside/\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


El texto del documento se envuelve en el lado de la forma que está más alejado del margen de la página, dejando un área libre de texto en el otro lado de la forma.

### LEFT {#LEFT}
```
public static int LEFT
```


El texto del documento se envuelve solo en el lado izquierdo de la forma. Hay un área libre de texto a la derecha de la forma.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


El texto del documento se envuelve solo en el lado derecho de la forma. Hay un área libre de texto a la izquierda de la forma.

### length {#length}
```
public static int length
```


### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
