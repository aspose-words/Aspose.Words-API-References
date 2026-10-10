---
title: "WrapSide"
linktitle: "WrapSide"
second_title: "Aspose.Words pour Java"
description: "Spécifie les côtés de la forme ou de l'image autour desquels le texte s'enroule en Java."
type: docs
weight: 736
url: /fr/java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

Spécifie de quel(s) côté(s) de la forme ou de l'image le texte s'enroule.

 **Examples:** 

Montre comment remplacer toutes les formes de zone de texte par des formes d'image.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTH](#BOTH) | Le texte du document s'enroule des deux côtés de la forme. |
| [DEFAULT](#DEFAULT) | La valeur par défaut est [BOTH](../../com.aspose.words/wrapside/\#BOTH). |
| [LARGEST](#LARGEST) | Le texte du document s'enroule du côté de la forme le plus éloigné de la marge de la page, laissant une zone libre de texte de l'autre côté de la forme. |
| [LEFT](#LEFT) | Le texte du document s'enroule uniquement du côté gauche de la forme. |
| [RIGHT](#RIGHT) | Le texte du document s'enroule uniquement du côté droit de la forme. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapSide)](#toString-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


Le texte du document s'enroule des deux côtés de la forme.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


La valeur par défaut est [BOTH](../../com.aspose.words/wrapside/\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


Le texte du document s'enroule du côté de la forme le plus éloigné de la marge de la page, laissant une zone libre de texte de l'autre côté de la forme.

### LEFT {#LEFT}
```
public static int LEFT
```


Le texte du document s'enroule uniquement du côté gauche de la forme. Il y a une zone libre de texte à droite de la forme.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Le texte du document s'enroule uniquement du côté droit de la forme. Il y a une zone libre de texte à gauche de la forme.

### length {#length}
```
public static int length
```


### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
