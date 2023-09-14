---
title: DashStyle
linktitle: DashStyle
second_title: Aspose.Words for Java
description: Dashed line style in Java.
type: docs
weight: 123
url: /java/com.aspose.words/dashstyle/
---

**Inheritance:**
java.lang.Object
```
public class DashStyle
```

Dashed line style.

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
| [DASH](#DASH) | Dash style. |
| [DASH_DOT](#DASH-DOT) | Dash short dash. |
| [DEFAULT](#DEFAULT) | Same as [SOLID](../../com.aspose.words/dashstyle/\#SOLID). |
| [DOT](#DOT) | Square dot style. |
| [LONG_DASH](#LONG-DASH) | Long dash style. |
| [LONG_DASH_DOT](#LONG-DASH-DOT) | Long dash short dash. |
| [LONG_DASH_DOT_DOT](#LONG-DASH-DOT-DOT) | Long dash short dash short dash. |
| [SHORT_DASH](#SHORT-DASH) | System dash style. |
| [SHORT_DASH_DOT](#SHORT-DASH-DOT) | System dash style. |
| [SHORT_DASH_DOT_DOT](#SHORT-DASH-DOT-DOT) | System dash style. |
| [SHORT_DOT](#SHORT-DOT) | System dash style. |
| [SOLID](#SOLID) | Solid (continuous) pen. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String dashStyleName)](#fromName-java.lang.String) |  |
| [getName(int dashStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dashStyle)](#toString-int) |  |
### DASH {#DASH}
```
public static int DASH
```


Dash style.

### DASH_DOT {#DASH-DOT}
```
public static int DASH_DOT
```


Dash short dash.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Same as [SOLID](../../com.aspose.words/dashstyle/\#SOLID).

### DOT {#DOT}
```
public static int DOT
```


Square dot style.

### LONG_DASH {#LONG-DASH}
```
public static int LONG_DASH
```


Long dash style.

### LONG_DASH_DOT {#LONG-DASH-DOT}
```
public static int LONG_DASH_DOT
```


Long dash short dash.

### LONG_DASH_DOT_DOT {#LONG-DASH-DOT-DOT}
```
public static int LONG_DASH_DOT_DOT
```


Long dash short dash short dash.

### SHORT_DASH {#SHORT-DASH}
```
public static int SHORT_DASH
```


System dash style.

### SHORT_DASH_DOT {#SHORT-DASH-DOT}
```
public static int SHORT_DASH_DOT
```


System dash style.

### SHORT_DASH_DOT_DOT {#SHORT-DASH-DOT-DOT}
```
public static int SHORT_DASH_DOT_DOT
```


System dash style.

### SHORT_DOT {#SHORT-DOT}
```
public static int SHORT_DOT
```


System dash style.

### SOLID {#SOLID}
```
public static int SOLID
```


Solid (continuous) pen.

### length {#length}
```
public static int length
```


### fromName(String dashStyleName) {#fromName-java.lang.String}
```
public static int fromName(String dashStyleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dashStyleName | java.lang.String |  |

**Returns:**
int
### getName(int dashStyle) {#getName-int}
```
public static String getName(int dashStyle)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| dashStyle | int |  |

**Returns:**
java.lang.String
