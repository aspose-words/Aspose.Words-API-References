---
title: "ArrowType"
linktitle: "ArrowType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'une flèche à l'extrémité d'une ligne en Java."
type: docs
weight: 18
url: /fr/java/com.aspose.words/arrowtype/
---

**Inheritance:**
java.lang.Object
```
public class ArrowType
```

Spécifie le type d'une flèche à l'extrémité d'une ligne.

 **Examples:** 

Permet de créer une variété de formes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are four examples of shapes that we can insert into our documents.
 // 1 -  Dotted, horizontal, half-transparent red line
 // with an arrow on the left end and a diamond on the right end:
 Shape arrow = new Shape(doc, ShapeType.LINE);
 arrow.setWidth(200.0);
 arrow.getStroke().setColor(Color.RED);
 arrow.getStroke().setStartArrowType(ArrowType.ARROW);
 arrow.getStroke().setStartArrowLength(ArrowLength.LONG);
 arrow.getStroke().setStartArrowWidth(ArrowWidth.WIDE);
 arrow.getStroke().setEndArrowType(ArrowType.DIAMOND);
 arrow.getStroke().setEndArrowLength(ArrowLength.LONG);
 arrow.getStroke().setEndArrowWidth(ArrowWidth.WIDE);
 arrow.getStroke().setDashStyle(DashStyle.DASH);
 arrow.getStroke().setOpacity(0.5);

 Assert.assertEquals(arrow.getStroke().getJoinStyle(), JoinStyle.MITER);

 builder.insertNode(arrow);

 // 2 -  Thick black diagonal line with rounded ends:
 Shape line = new Shape(doc, ShapeType.LINE);
 line.setTop(40.0);
 line.setWidth(200.0);
 line.setHeight(20.0);
 line.setStrokeWeight(5.0);
 line.getStroke().setEndCap(EndCap.ROUND);

 builder.insertNode(line);

 // 3 -  Arrow with a green fill:
 Shape filledInArrow = new Shape(doc, ShapeType.ARROW);
 filledInArrow.setWidth(200.0);
 filledInArrow.setHeight(40.0);
 filledInArrow.setTop(100.0);
 filledInArrow.getFill().setForeColor(Color.GREEN);
 filledInArrow.getFill().setVisible(true);

 builder.insertNode(filledInArrow);

 // 4 -  Arrow with a flipped orientation filled in with the Aspose logo:
 Shape filledInArrowImg = new Shape(doc, ShapeType.ARROW);
 filledInArrowImg.setWidth(200.0);
 filledInArrowImg.setHeight(40.0);
 filledInArrowImg.setTop(160.0);
 filledInArrowImg.setFlipOrientation(FlipOrientation.BOTH);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());
 Graphics2D graphics2D = image.createGraphics();

 // When we flip the orientation of our arrow, we also flip the image that the arrow contains.
 // Flip the image the other way to cancel this out before getting the shape to display it.
 AffineTransform at = new AffineTransform();
 at.concatenate(AffineTransform.getScaleInstance(1, -1));
 at.concatenate(AffineTransform.getTranslateInstance(0, -image.getHeight()));
 graphics2D.transform(at);
 graphics2D.drawImage(image, 0, 0, null);
 graphics2D.dispose();

 filledInArrowImg.getImageData().setImage(image);
 builder.insertNode(filledInArrowImg);

 doc.save(getArtifactsDir() + "Drawing.VariousShapes.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ARROW](#ARROW) | La flèche est un triangle plein. |
| [DEFAULT](#DEFAULT) | Identique à [NONE](../../com.aspose.words/arrowtype/\#NONE). |
| [DIAMOND](#DIAMOND) | L'extrémité de la ligne est un losange plein. |
| [NONE](#NONE) | La ligne n'a pas de flèche à l'extrémité. |
| [OPEN](#OPEN) | La flèche est une flèche ouverte. |
| [OVAL](#OVAL) | L'extrémité de la ligne est un ovale plein. |
| [STEALTH](#STEALTH) | La flèche est une flèche \"stealth\". |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String arrowTypeName)](#fromName-java.lang.String) |  |
| [getName(int arrowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int arrowType)](#toString-int) |  |
### ARROW {#ARROW}
```
public static int ARROW
```


La flèche est un triangle plein.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Identique à [NONE](../../com.aspose.words/arrowtype/\#NONE).

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


L'extrémité de la ligne est un losange plein.

### NONE {#NONE}
```
public static int NONE
```


La ligne n'a pas de flèche à l'extrémité.

### OPEN {#OPEN}
```
public static int OPEN
```


La flèche est une flèche ouverte.

### OVAL {#OVAL}
```
public static int OVAL
```


L'extrémité de la ligne est un ovale plein.

### STEALTH {#STEALTH}
```
public static int STEALTH
```


La flèche est une flèche \"stealth\".

### length {#length}
```
public static int length
```


### fromName(String arrowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String arrowTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| arrowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int arrowType) {#getName-int}
```
public static String getName(int arrowType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| arrowType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int arrowType) {#toString-int}
```
public static String toString(int arrowType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| arrowType | int |  |

**Returns:**
java.lang.String
