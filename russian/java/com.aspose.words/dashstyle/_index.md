---
title: "DashStyle"
linktitle: "DashStyle"
second_title: "Aspose.Words для Java"
description: "Стиль пунктирной линии в Java."
type: docs
weight: 148
url: /ru/java/com.aspose.words/dashstyle/
---

**Inheritance:**
java.lang.Object
```
public class DashStyle
```

Стиль пунктирной линии.

 **Examples:** 

Показывает, как создавать разнообразные фигуры.

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
## Поля

| Поле | Описание |
| --- | --- |
| [DASH](#DASH) | Стиль штриха. |
| [DASH_DOT](#DASH-DOT) | Тире короткое тире. |
| [DEFAULT](#DEFAULT) | То же, что и [SOLID](../../com.aspose.words/dashstyle/\#SOLID). |
| [DOT](#DOT) | Стиль квадратных точек. |
| [LONG_DASH](#LONG-DASH) | Стиль длинного тире. |
| [LONG_DASH_DOT](#LONG-DASH-DOT) | Длинное тире короткое тире. |
| [LONG_DASH_DOT_DOT](#LONG-DASH-DOT-DOT) | Длинное тире короткое тире короткое тире. |
| [SHORT_DASH](#SHORT-DASH) | Системный стиль тире. |
| [SHORT_DASH_DOT](#SHORT-DASH-DOT) | Системный стиль тире. |
| [SHORT_DASH_DOT_DOT](#SHORT-DASH-DOT-DOT) | Системный стиль тире. |
| [SHORT_DOT](#SHORT-DOT) | Системный стиль тире. |
| [SOLID](#SOLID) | Сплошная (непрерывная) ручка. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String dashStyleName)](#fromName-java.lang.String) |  |
| [getName(int dashStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dashStyle)](#toString-int) |  |
### DASH {#DASH}
```
public static int DASH
```


Стиль штриха.

### DASH_DOT {#DASH-DOT}
```
public static int DASH_DOT
```


Тире короткое тире.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


То же, что и [SOLID](../../com.aspose.words/dashstyle/\#SOLID).

### DOT {#DOT}
```
public static int DOT
```


Стиль квадратных точек.

### LONG_DASH {#LONG-DASH}
```
public static int LONG_DASH
```


Стиль длинного тире.

### LONG_DASH_DOT {#LONG-DASH-DOT}
```
public static int LONG_DASH_DOT
```


Длинное тире короткое тире.

### LONG_DASH_DOT_DOT {#LONG-DASH-DOT-DOT}
```
public static int LONG_DASH_DOT_DOT
```


Длинное тире короткое тире короткое тире.

### SHORT_DASH {#SHORT-DASH}
```
public static int SHORT_DASH
```


Системный стиль тире.

### SHORT_DASH_DOT {#SHORT-DASH-DOT}
```
public static int SHORT_DASH_DOT
```


Системный стиль тире.

### SHORT_DASH_DOT_DOT {#SHORT-DASH-DOT-DOT}
```
public static int SHORT_DASH_DOT_DOT
```


Системный стиль тире.

### SHORT_DOT {#SHORT-DOT}
```
public static int SHORT_DOT
```


Системный стиль тире.

### SOLID {#SOLID}
```
public static int SOLID
```


Сплошная (непрерывная) ручка.

### length {#length}
```
public static int length
```


### fromName(String dashStyleName) {#fromName-java.lang.String}
```
public static int fromName(String dashStyleName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dashStyleName | java.lang.String |  |

**Returns:**
int
### getName(int dashStyle) {#getName-int}
```
public static String getName(int dashStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| dashStyle | int |  |

**Returns:**
java.lang.String
