---
title: "WrapSide"
linktitle: "WrapSide"
second_title: "Aspose.Words für Java"
description: "Gibt an, an welchen Seiten der Form oder des Bildes der Text in Java umfließt."
type: docs
weight: 736
url: /de/java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

Gibt an, an welcher Seite(n) der Form oder des Bildes der Text umfließt.

 **Examples:** 

Zeigt, wie man alle Textfeldformen durch Bildformen ersetzt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOTH](#BOTH) | Der Dokumenttext umfließt beide Seiten der Form. |
| [DEFAULT](#DEFAULT) | Standardwert ist [BOTH](../../com.aspose.words/wrapside/\#BOTH). |
| [LARGEST](#LARGEST) | Der Dokumenttext umfließt die Seite der Form, die am weitesten vom Seitenrand entfernt ist, und lässt auf der anderen Seite der Form einen freien Textbereich. |
| [LEFT](#LEFT) | Der Dokumenttext umfließt nur die linke Seite der Form. |
| [RIGHT](#RIGHT) | Der Dokumenttext umfließt nur die rechte Seite der Form. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapSide)](#toString-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


Der Dokumenttext umfließt beide Seiten der Form.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert ist [BOTH](../../com.aspose.words/wrapside/\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


Der Dokumenttext umfließt die Seite der Form, die am weitesten vom Seitenrand entfernt ist, und lässt auf der anderen Seite der Form einen freien Textbereich.

### LEFT {#LEFT}
```
public static int LEFT
```


Der Dokumenttext umfließt nur die linke Seite der Form. Auf der rechten Seite der Form gibt es einen freien Textbereich.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Der Dokumenttext umfließt nur die rechte Seite der Form. Auf der linken Seite der Form gibt es einen freien Textbereich.

### length {#length}
```
public static int length
```


### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
