---
title: EndCap
linktitle: EndCap
second_title: Aspose.Words for Java
description: Specifies line cap style in Java.
type: docs
weight: 188
url: /java/com.aspose.words/endcap/
---

**Inheritance:**
java.lang.Object
```
public class EndCap
```

Specifies line cap style.

 **Examples:** 

Shows to create a variety of shapes.

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

 BufferedImage image = ImageIO.read(getAsposelogoUri().toURL().openStream());
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
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Default value is [FLAT](../../com.aspose.words/endcap/\#FLAT). |
| [FLAT](#FLAT) | Line ends at end point. |
| [ROUND](#ROUND) | Rounded ends. |
| [SQUARE](#SQUARE) | Square protrudes by half line width. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String endCapName)](#fromName-java.lang.String) |  |
| [getName(int endCap)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int endCap)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value is [FLAT](../../com.aspose.words/endcap/\#FLAT).

### FLAT {#FLAT}
```
public static int FLAT
```


Line ends at end point.

### ROUND {#ROUND}
```
public static int ROUND
```


Rounded ends.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Square protrudes by half line width.

### length {#length}
```
public static int length
```


### fromName(String endCapName) {#fromName-java.lang.String}
```
public static int fromName(String endCapName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| endCapName | java.lang.String |  |

**Returns:**
int
### getName(int endCap) {#getName-int}
```
public static String getName(int endCap)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| endCap | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int endCap) {#toString-int}
```
public static String toString(int endCap)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| endCap | int |  |

**Returns:**
java.lang.String
