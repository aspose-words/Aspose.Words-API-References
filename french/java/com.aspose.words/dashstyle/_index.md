---
title: "DashStyle"
linktitle: "DashStyle"
second_title: "Aspose.Words pour Java"
description: "Style de ligne pointillée en Java."
type: docs
weight: 148
url: /fr/java/com.aspose.words/dashstyle/
---

**Inheritance:**
java.lang.Object
```
public class DashStyle
```

Style de ligne pointillée.

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
| [DASH](#DASH) | Style de tiret. |
| [DASH_DOT](#DASH-DOT) | Tiret court. |
| [DEFAULT](#DEFAULT) | Identique à [SOLID](../../com.aspose.words/dashstyle/\#SOLID). |
| [DOT](#DOT) | Style point carré. |
| [LONG_DASH](#LONG-DASH) | Style tiret long. |
| [LONG_DASH_DOT](#LONG-DASH-DOT) | Tiret long court. |
| [LONG_DASH_DOT_DOT](#LONG-DASH-DOT-DOT) | Tiret long court court. |
| [SHORT_DASH](#SHORT-DASH) | Style de tiret système. |
| [SHORT_DASH_DOT](#SHORT-DASH-DOT) | Style de tiret système. |
| [SHORT_DASH_DOT_DOT](#SHORT-DASH-DOT-DOT) | Style de tiret système. |
| [SHORT_DOT](#SHORT-DOT) | Style de tiret système. |
| [SOLID](#SOLID) | Stylo plein (continu). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String dashStyleName)](#fromName-java.lang.String) |  |
| [getName(int dashStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dashStyle)](#toString-int) |  |
### DASH {#DASH}
```
public static int DASH
```


Style de tiret.

### DASH_DOT {#DASH-DOT}
```
public static int DASH_DOT
```


Tiret court.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Identique à [SOLID](../../com.aspose.words/dashstyle/\#SOLID).

### DOT {#DOT}
```
public static int DOT
```


Style point carré.

### LONG_DASH {#LONG-DASH}
```
public static int LONG_DASH
```


Style tiret long.

### LONG_DASH_DOT {#LONG-DASH-DOT}
```
public static int LONG_DASH_DOT
```


Tiret long court.

### LONG_DASH_DOT_DOT {#LONG-DASH-DOT-DOT}
```
public static int LONG_DASH_DOT_DOT
```


Tiret long court court.

### SHORT_DASH {#SHORT-DASH}
```
public static int SHORT_DASH
```


Style de tiret système.

### SHORT_DASH_DOT {#SHORT-DASH-DOT}
```
public static int SHORT_DASH_DOT
```


Style de tiret système.

### SHORT_DASH_DOT_DOT {#SHORT-DASH-DOT-DOT}
```
public static int SHORT_DASH_DOT_DOT
```


Style de tiret système.

### SHORT_DOT {#SHORT-DOT}
```
public static int SHORT_DOT
```


Style de tiret système.

### SOLID {#SOLID}
```
public static int SOLID
```


Stylo plein (continu).

### length {#length}
```
public static int length
```


### fromName(String dashStyleName) {#fromName-java.lang.String}
```
public static int fromName(String dashStyleName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dashStyleName | java.lang.String |  |

**Returns:**
int
### getName(int dashStyle) {#getName-int}
```
public static String getName(int dashStyle)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dashStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dashStyle) {#toString-int}
```
public static String toString(int dashStyle)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dashStyle | int |  |

**Returns:**
java.lang.String
