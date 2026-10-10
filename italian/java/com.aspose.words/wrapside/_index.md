---
title: "WrapSide"
linktitle: "WrapSide"
second_title: "Aspose.Words per Java"
description: "Specifica su quali lati della forma o dell'immagine il testo avvolge in Java."
type: docs
weight: 736
url: /it/java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

Specifica su quale lato (i) della forma o dell'immagine il testo si avvolge.

 **Examples:** 

Mostra come sostituire tutte le forme di casella di testo con forme immagine.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTH](#BOTH) | Il testo del documento avvolge entrambi i lati della forma. |
| [DEFAULT](#DEFAULT) | Il valore predefinito è [BOTH](../../com.aspose.words/wrapside/\#BOTH). |
| [LARGEST](#LARGEST) | Il testo del documento avvolge il lato della forma più lontano dal margine della pagina, lasciando un'area libera di testo sull'altro lato della forma. |
| [LEFT](#LEFT) | Il testo del documento avvolge solo il lato sinistro della forma. |
| [RIGHT](#RIGHT) | Il testo del documento avvolge solo il lato destro della forma. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapSide)](#toString-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


Il testo del documento avvolge entrambi i lati della forma.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il valore predefinito è [BOTH](../../com.aspose.words/wrapside/\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


Il testo del documento avvolge il lato della forma più lontano dal margine della pagina, lasciando un'area libera di testo sull'altro lato della forma.

### LEFT {#LEFT}
```
public static int LEFT
```


Il testo del documento avvolge solo il lato sinistro della forma. C'è un'area libera di testo sul lato destro della forma.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Il testo del documento avvolge solo il lato destro della forma. C'è un'area libera di testo sul lato sinistro della forma.

### length {#length}
```
public static int length
```


### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
