---
title: "Заливка"
linktitle: "Заливка"
second_title: "Aspose.Words для Java"
description: "Представляет форматирование заливки для объекта в Java."
type: docs
weight: 311
url: /ru/java/com.aspose.words/fill/
---

**Inheritance:**
java.lang.Object
```
public class Fill
```

Представляет формат заполнения для объекта.

Чтобы узнать больше, посетите статью документации [ Working with Graphic Elements ][Working with Graphic Elements].

 **Remarks:** 

Используйте свойство [ShapeBase.getFill()](../../com.aspose.words/shapebase/\#getFill) или [Font.getFill()](../../com.aspose.words/font/\#getFill) для доступа к свойствам заливки объекта. Вы не создаёте экземпляры класса [Fill](../../com.aspose.words/fill/) напрямую.

 **Examples:** 

Показывает, как заполнить форму сплошным цветом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Методы

| Метод | Описание |
| --- | --- |
| [getBackColor()](#getBackColor) | Возвращает объект Color, представляющий цвет фона заливки. |
| [getBackThemeColor()](#getBackThemeColor) | Возвращает объект ThemeColor, представляющий цвет фона заливки. |
| [getBackTintAndShade()](#getBackTintAndShade) | Возвращает значение double, которое осветляет или затемняет цвет фона. |
| [getBaseForeColor()](#getBaseForeColor) | Возвращает объект Color, представляющий базовый цвет переднего плана заливки без каких-либо модификаторов. |
| [getColor()](#getColor) | Возвращает объект Color, представляющий цвет переднего плана заливки. |
| [getFillType()](#getFillType) | Возвращает тип заливки. |
| [getForeColor()](#getForeColor) | Возвращает объект Color, представляющий цвет переднего плана заливки. |
| [getForeThemeColor()](#getForeThemeColor) | Возвращает объект ThemeColor, представляющий цвет переднего плана заливки. |
| [getForeTintAndShade()](#getForeTintAndShade) | Возвращает значение double, которое осветляет или затемняет цвет переднего плана. |
| [getGradientAngle()](#getGradientAngle) | Возвращает угол градиентной заливки. |
| [getGradientStops()](#getGradientStops) | Возвращает коллекцию объектов [GradientStop](../../com.aspose.words/gradientstop/) для заливки. |
| [getGradientStyle()](#getGradientStyle) | Получает стиль градиента [GradientStyle](../../com.aspose.words/gradientstyle/) для заливки. |
| [getGradientVariant()](#getGradientVariant) | Получает вариант градиента [GradientVariant](../../com.aspose.words/gradientvariant/) для заливки. |
| [getImageBytes()](#getImageBytes) | Получает необработанные байты текстуры или узора заливки. |
| [getOpacity()](#getOpacity) | Получает степень непрозрачности указанной заливки в виде значения от 0.0 (прозрачная) до 1.0 (непрозрачная). |
| [getPattern()](#getPattern) | Получает [PatternType](../../com.aspose.words/patterntype/) для заливки. |
| [getPresetTexture()](#getPresetTexture) | Получает [PresetTexture](../../com.aspose.words/presettexture/) для заливки. |
| [getRotateWithObject()](#getRotateWithObject) | Получает, вращается ли заливка вместе с указанным объектом. |
| [getTextureAlignment()](#getTextureAlignment) | Получает выравнивание для заливки плиточной текстурой. |
| [getTransparency()](#getTransparency) | Получает степень прозрачности указанной заливки в виде значения от 0.0 (непрозрачная) до 1.0 (прозрачная). |
| [getVisible()](#getVisible) | Получает значение, которое является  true  если форматирование, применённое к этому экземпляру, видно. |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [patterned(int patternType, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Устанавливает объект Color, представляющий цвет фона заливки. |
| [setBackThemeColor(int value)](#setBackThemeColor-int) | Устанавливает объект ThemeColor, представляющий цвет фона заливки. |
| [setBackTintAndShade(double value)](#setBackTintAndShade-double) | Устанавливает значение типа double, которое осветляет или затемняет цвет фона. |
| [setColor(Color value)](#setColor-java.awt.Color) | Устанавливает объект Color, представляющий цвет переднего плана заливки. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Устанавливает объект Color, представляющий цвет переднего плана заливки. |
| [setForeThemeColor(int value)](#setForeThemeColor-int) | Устанавливает объект ThemeColor, представляющий цвет переднего плана заливки. |
| [setForeTintAndShade(double value)](#setForeTintAndShade-double) | Устанавливает значение типа double, которое осветляет или затемняет цвет переднего плана. |
| [setGradientAngle(double value)](#setGradientAngle-double) | Устанавливает угол градиентной заливки. |
| [setImage(byte[] imageBytes)](#setImage-byte) | Изменяет тип заливки на одиночное изображение. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Изменяет тип заливки на одиночное изображение. |
| [setOpacity(double value)](#setOpacity-double) | Устанавливает степень непрозрачности указанной заливки в виде значения от 0.0 (прозрачная) до 1.0 (непрозрачная). |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) | Устанавливает, вращается ли заливка вместе с указанным объектом. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) | Устанавливает выравнивание для заливки плиточной текстурой. |
| [setTransparency(double value)](#setTransparency-double) | Устанавливает степень прозрачности указанной заливки в виде значения от 0.0 (непрозрачная) до 1.0 (прозрачная). |
| [setVisible(boolean value)](#setVisible-boolean) | Устанавливает значение, которое является  true  если форматирование, применённое к этому экземпляру, видно. |
| [solid()](#solid) | Устанавливает заливку в единый цвет. |
| [solid(Color color)](#solid-java.awt.Color) | Устанавливает заливку в указанный единый цвет. |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int) |  |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Возвращает объект Color, представляющий цвет фона заливки.

 **Examples:** 

Показывает, как заполнить форму градиентом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```

**Returns:**
java.awt.Color - Объект Color, представляющий цвет фона для заливки.
### getBackThemeColor() {#getBackThemeColor}
```
public int getBackThemeColor()
```


Возвращает объект ThemeColor, представляющий цвет фона заливки.

 **Examples:** 

Показывает, как установить тематический цвет для переднего/заднего цвета фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ROUND_RECTANGLE, 80.0, 80.0);

 Fill fill = shape.getFill();
 fill.setForeThemeColor(ThemeColor.DARK_1);
 fill.setBackThemeColor(ThemeColor.BACKGROUND_2);

 // Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
 if (fill.getBackTintAndShade() == 0)
     fill.setBackTintAndShade(0.2);

 doc.save(getArtifactsDir() + "Shape.FillThemeColor.docx");
 
```

**Returns:**
int - Объект ThemeColor, представляющий цвет фона для заливки. Возвращаемое значение является одной из констант [ThemeColor](../../com.aspose.words/themecolor/).
### getBackTintAndShade() {#getBackTintAndShade}
```
public double getBackTintAndShade()
```


Возвращает значение double, которое осветляет или затемняет цвет фона.

**Returns:**
double - Значение типа double, которое осветляет или затемняет цвет фона.
### getBaseForeColor() {#getBaseForeColor}
```
public Color getBaseForeColor()
```


Возвращает объект Color, представляющий базовый цвет переднего плана заливки без каких-либо модификаторов.

 **Examples:** 

Показывает, как получить цвет переднего плана без модификаторов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 shape.getFill().setForeColor(Color.RED);
 shape.getFill().setForeTintAndShade(0.5);
 shape.getStroke().getFill().setForeColor(Color.GREEN);
 shape.getStroke().getFill().setTransparency(0.5);

 Assert.assertEquals(new Color((255), (188), (188), (255)).getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getBaseForeColor().getRGB());

 Assert.assertEquals(new Color((0), (255), (0), (128)).getRGB(), shape.getStroke().getForeColor().getRGB());
 Assert.assertEquals(Color.GREEN.getRGB(), shape.getStroke().getBaseForeColor().getRGB());

 Assert.assertEquals(Color.GREEN.getRGB(), shape.getStroke().getFill().getForeColor().getRGB());
 Assert.assertEquals(Color.GREEN.getRGB(), shape.getStroke().getFill().getBaseForeColor().getRGB());
 
```

**Returns:**
java.awt.Color - Объект Color, представляющий базовый цвет переднего плана для заливки без каких-либо модификаторов.
### getColor() {#getColor}
```
public Color getColor()
```


Возвращает объект Color, представляющий цвет переднего плана заливки.

 **Remarks:** 

Это свойство сохраняет альфа‑компонент java.awt.Color, в отличие от свойства [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color), которое сбрасывает его до полностью непрозрачного цвета.

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Returns:**
java.awt.Color - Объект Color, представляющий цвет переднего плана для заливки.
### getFillType() {#getFillType}
```
public int getFillType()
```


Возвращает тип заливки.

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Returns:**
int - Тип заливки. Возвращаемое значение является одной из констант [FillType](../../com.aspose.words/filltype/).
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Возвращает объект Color, представляющий цвет переднего плана заливки.

 **Remarks:** 

Это свойство сбрасывает альфа‑компонент java.awt.Color до полностью непрозрачного цвета, в отличие от свойства [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color), которое сохраняет его.

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

**Returns:**
java.awt.Color - Объект Color, представляющий цвет переднего плана для заливки.
### getForeThemeColor() {#getForeThemeColor}
```
public int getForeThemeColor()
```


Возвращает объект ThemeColor, представляющий цвет переднего плана заливки.

 **Examples:** 

Показывает, как установить тематический цвет для переднего/заднего цвета фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ROUND_RECTANGLE, 80.0, 80.0);

 Fill fill = shape.getFill();
 fill.setForeThemeColor(ThemeColor.DARK_1);
 fill.setBackThemeColor(ThemeColor.BACKGROUND_2);

 // Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
 if (fill.getBackTintAndShade() == 0)
     fill.setBackTintAndShade(0.2);

 doc.save(getArtifactsDir() + "Shape.FillThemeColor.docx");
 
```

**Returns:**
int - Объект ThemeColor, представляющий цвет переднего плана для заливки. Возвращаемое значение является одной из констант [ThemeColor](../../com.aspose.words/themecolor/).
### getForeTintAndShade() {#getForeTintAndShade}
```
public double getForeTintAndShade()
```


Возвращает значение double, которое осветляет или затемняет цвет переднего плана.

**Returns:**
double - Значение типа double, которое осветляет или затемняет цвет переднего плана.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```


Возвращает угол градиентной заливки.

 **Examples:** 

Показывает, как заполнить форму градиентом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```

**Returns:**
double - Угол градиентной заливки.
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```


Возвращает коллекцию объектов [GradientStop](../../com.aspose.words/gradientstop/) для заливки.

 **Examples:** 

Показывает, как добавить градиентные остановки к градиентной заливке.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/) - A collection of [GradientStop](../../com.aspose.words/gradientstop/) objects for the fill.
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```


Получает стиль градиента [GradientStyle](../../com.aspose.words/gradientstyle/) для заливки.

 **Examples:** 

Показывает, как заполнить форму градиентом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```

**Returns:**
int - Стиль градиента [GradientStyle](../../com.aspose.words/gradientstyle/) для заливки. Возвращаемое значение является одной из констант [GradientStyle](../../com.aspose.words/gradientstyle/).
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```


Получает вариант градиента [GradientVariant](../../com.aspose.words/gradientvariant/) для заливки.

 **Examples:** 

Показывает, как заполнить форму градиентом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```

**Returns:**
int - Вариант градиента [GradientVariant](../../com.aspose.words/gradientvariant/) для заливки. Возвращаемое значение является одной из констант [GradientVariant](../../com.aspose.words/gradientvariant/).
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Получает необработанные байты текстуры или узора заливки.

 **Remarks:** 

Значение по умолчанию равно  null .

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

**Returns:**
byte[] - Необработанные байты текстуры или узора заливки.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


Получает степень непрозрачности указанной заливки в виде значения от 0.0 (прозрачная) до 1.0 (непрозрачная).

 **Remarks:** 

Это свойство является противоположным свойству [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Показывает, как заполнить форму сплошным цветом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```

**Returns:**
double - Степень непрозрачности указанной заливки в виде значения от 0.0 (прозрачный) до 1.0 (непрозрачный).
### getPattern() {#getPattern}
```
public int getPattern()
```


Получает [PatternType](../../com.aspose.words/patterntype/) для заливки.

 **Examples:** 

Показывает, как установить узор для фигуры.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Fill fill = shape.getFill();

 System.out.println(MessageFormat.format("Pattern value is: {0}",fill.getPattern()));

 // There are several ways specified fill to a pattern.
 // 1 -  Apply pattern to the shape fill:
 fill.patterned(PatternType.DIAGONAL_BRICK);

 // 2 -  Apply pattern with foreground and background colors to the shape fill:
 fill.patterned(PatternType.DIAGONAL_BRICK, Color.yellow, Color.blue);

 doc.save(getArtifactsDir() + "Shape.FillPattern.docx");
 
```

**Returns:**
int - [PatternType](../../com.aspose.words/patterntype/) для заливки. Возвращаемое значение является одной из констант [PatternType](../../com.aspose.words/patterntype/).
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```


Получает [PresetTexture](../../com.aspose.words/presettexture/) для заливки.

 **Examples:** 

Показывает, как заполнять и замощать текстуру внутри фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);

 // Apply texture alignment to the shape fill.
 shape.getFill().presetTextured(PresetTexture.CANVAS);
 shape.getFill().setTextureAlignment(TextureAlignment.TOP_RIGHT);

 // Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
 // property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.TextureFill.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "Shape.TextureFill.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals(TextureAlignment.TOP_RIGHT, shape.getFill().getTextureAlignment());
 Assert.assertEquals(PresetTexture.CANVAS, shape.getFill().getPresetTexture());
 
```

**Returns:**
int - [PresetTexture](../../com.aspose.words/presettexture/) для заливки. Возвращаемое значение является одной из констант [PresetTexture](../../com.aspose.words/presettexture/).
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```


Получает, вращается ли заливка вместе с указанным объектом.

**Returns:**
boolean - Определяет, вращается ли заливка вместе с указанным объектом.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```


Получает выравнивание для заливки плиточной текстурой.

 **Examples:** 

Показывает, как заполнять и замощать текстуру внутри фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);

 // Apply texture alignment to the shape fill.
 shape.getFill().presetTextured(PresetTexture.CANVAS);
 shape.getFill().setTextureAlignment(TextureAlignment.TOP_RIGHT);

 // Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
 // property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.TextureFill.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "Shape.TextureFill.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals(TextureAlignment.TOP_RIGHT, shape.getFill().getTextureAlignment());
 Assert.assertEquals(PresetTexture.CANVAS, shape.getFill().getPresetTexture());
 
```

**Returns:**
int - Выравнивание для плиточной текстурной заливки. Возвращаемое значение является одной из констант [TextureAlignment](../../com.aspose.words/texturealignment/).
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Получает степень прозрачности указанной заливки в виде значения от 0.0 (непрозрачная) до 1.0 (прозрачная).

 **Remarks:** 

Это свойство является противоположным свойству [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Returns:**
double - Степень прозрачности указанного заполнения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Получает значение, которое является  true  если форматирование, применённое к этому экземпляру, видно.

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

**Returns:**
boolean - Значение, которое является  true  если форматирование, применённое к этому экземпляру, видно.
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| стиль | int |  |
| variant | int |  |
| degree | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| color | java.awt.Color |  |
| стиль | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |

### patterned(int patternType, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color}
```
public void patterned(int patternType, Color foreColor, Color backColor)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Устанавливает объект Color, представляющий цвет фона заливки.

 **Examples:** 

Показывает, как заполнить форму градиентом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Объект Color, представляющий цвет фона для заполнения. |

### setBackThemeColor(int value) {#setBackThemeColor-int}
```
public void setBackThemeColor(int value)
```


Устанавливает объект ThemeColor, представляющий цвет фона заливки.

 **Examples:** 

Показывает, как установить тематический цвет для переднего/заднего цвета фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ROUND_RECTANGLE, 80.0, 80.0);

 Fill fill = shape.getFill();
 fill.setForeThemeColor(ThemeColor.DARK_1);
 fill.setBackThemeColor(ThemeColor.BACKGROUND_2);

 // Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
 if (fill.getBackTintAndShade() == 0)
     fill.setBackTintAndShade(0.2);

 doc.save(getArtifactsDir() + "Shape.FillThemeColor.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Объект ThemeColor, представляющий цвет фона для заполнения. Значение должно быть одним из констант [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackTintAndShade(double value) {#setBackTintAndShade-double}
```
public void setBackTintAndShade(double value)
```


Устанавливает значение типа double, которое осветляет или затемняет цвет фона.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение double, которое осветляет или затемняет цвет фона. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Устанавливает объект Color, представляющий цвет переднего плана заливки.

 **Remarks:** 

Это свойство сохраняет альфа‑компонент java.awt.Color, в отличие от свойства [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color), которое сбрасывает его до полностью непрозрачного цвета.

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Объект Color, представляющий цвет переднего плана для заполнения. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Устанавливает объект Color, представляющий цвет переднего плана заливки.

 **Remarks:** 

Это свойство сбрасывает альфа‑компонент java.awt.Color до полностью непрозрачного цвета, в отличие от свойства [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color), которое сохраняет его.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Объект Color, представляющий цвет переднего плана для заполнения. |

### setForeThemeColor(int value) {#setForeThemeColor-int}
```
public void setForeThemeColor(int value)
```


Устанавливает объект ThemeColor, представляющий цвет переднего плана заливки.

 **Examples:** 

Показывает, как установить тематический цвет для переднего/заднего цвета фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ROUND_RECTANGLE, 80.0, 80.0);

 Fill fill = shape.getFill();
 fill.setForeThemeColor(ThemeColor.DARK_1);
 fill.setBackThemeColor(ThemeColor.BACKGROUND_2);

 // Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
 if (fill.getBackTintAndShade() == 0)
     fill.setBackTintAndShade(0.2);

 doc.save(getArtifactsDir() + "Shape.FillThemeColor.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Объект ThemeColor, представляющий цвет переднего плана для заполнения. Значение должно быть одним из констант [ThemeColor](../../com.aspose.words/themecolor/). |

### setForeTintAndShade(double value) {#setForeTintAndShade-double}
```
public void setForeTintAndShade(double value)
```


Устанавливает значение типа double, которое осветляет или затемняет цвет переднего плана.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение double, которое осветляет или затемняет цвет переднего плана. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```


Устанавливает угол градиентной заливки.

 **Examples:** 

Показывает, как заполнить форму градиентом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Угол градиентного заполнения. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```


Изменяет тип заливки на одиночное изображение.

 **Examples:** 

Показывает, как установить тип заполнения фигуры как изображение.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There are several ways of setting image.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // 1 -  Using a local system filename:
 shape.getFill().setImage(getImageDir() + "Logo.jpg");
 doc.save(getArtifactsDir() + "Shape.FillImage.FileName.docx");

 // 2 -  Load a file into a byte array:
 shape.getFill().setImage(Files.readAllBytes(Paths.get(getImageDir() + "Logo.jpg")));
 doc.save(getArtifactsDir() + "Shape.FillImage.ByteArray.docx");

 // 3 -  From a stream:
 FileInputStream stream = new FileInputStream(getImageDir() + "Logo.jpg");
 try
 {
     shape.getFill().setImage(stream);
 }
 finally { if (stream != null) stream.close(); }
 doc.save(getArtifactsDir() + "Shape.FillImage.Stream.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] | Массив байтов изображения. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Изменяет тип заливки на одиночное изображение.

 **Examples:** 

Показывает, как установить тип заполнения фигуры как изображение.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There are several ways of setting image.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // 1 -  Using a local system filename:
 shape.getFill().setImage(getImageDir() + "Logo.jpg");
 doc.save(getArtifactsDir() + "Shape.FillImage.FileName.docx");

 // 2 -  Load a file into a byte array:
 shape.getFill().setImage(Files.readAllBytes(Paths.get(getImageDir() + "Logo.jpg")));
 doc.save(getArtifactsDir() + "Shape.FillImage.ByteArray.docx");

 // 3 -  From a stream:
 FileInputStream stream = new FileInputStream(getImageDir() + "Logo.jpg");
 try
 {
     shape.getFill().setImage(stream);
 }
 finally { if (stream != null) stream.close(); }
 doc.save(getArtifactsDir() + "Shape.FillImage.Stream.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Путь к файлу изображения. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


Устанавливает степень непрозрачности указанной заливки в виде значения от 0.0 (прозрачная) до 1.0 (непрозрачная).

 **Remarks:** 

Это свойство является противоположным свойству [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Показывает, как заполнить форму сплошным цветом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Степень непрозрачности указанного заполнения в виде значения от 0.0 (прозрачный) до 1.0 (непрозрачный). |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```


Устанавливает, вращается ли заливка вместе с указанным объектом.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Определяет, вращается ли заполнение вместе с указанным объектом. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```


Устанавливает выравнивание для заливки плиточной текстурой.

 **Examples:** 

Показывает, как заполнять и замощать текстуру внутри фигуры.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);

 // Apply texture alignment to the shape fill.
 shape.getFill().presetTextured(PresetTexture.CANVAS);
 shape.getFill().setTextureAlignment(TextureAlignment.TOP_RIGHT);

 // Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
 // property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.TextureFill.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "Shape.TextureFill.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals(TextureAlignment.TOP_RIGHT, shape.getFill().getTextureAlignment());
 Assert.assertEquals(PresetTexture.CANVAS, shape.getFill().getPresetTexture());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Выравнивание для заполнения плиточной текстурой. Значение должно быть одним из констант [TextureAlignment](../../com.aspose.words/texturealignment/). |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Устанавливает степень прозрачности указанной заливки в виде значения от 0.0 (непрозрачная) до 1.0 (прозрачная).

 **Remarks:** 

Это свойство является противоположным свойству [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Степень прозрачности указанного заполнения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный). |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


Устанавливает значение, которое является  true  если форматирование, применённое к этому экземпляру, видно.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, которое является  true  если форматирование, применённое к этому экземпляру, видно. |

### solid() {#solid}
```
public void solid()
```


Устанавливает заливку в единый цвет.

 **Remarks:** 

Используйте этот метод, чтобы преобразовать любые заполнения обратно в сплошное заполнение.

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

### solid(Color color) {#solid-java.awt.Color}
```
public void solid(Color color)
```


Устанавливает заливку в указанный единый цвет.

 **Remarks:** 

Используйте этот метод, чтобы преобразовать любые заполнения обратно в сплошное заполнение.

 **Examples:** 

Показывает, как использовать форматирование диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete series generated by default.
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2" };
 series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });

 // Format chart background.
 chart.getFormat().getFill().solid(Color.darkGray);

 // Hide axis tick labels.
 chart.getAxisX().getTickLabels().setPosition(AxisTickLabelPosition.NONE);
 chart.getAxisY().getTickLabels().setPosition(AxisTickLabelPosition.NONE);

 // Format chart title.
 chart.getTitle().getFormat().getFill().solid(Color.yellow);

 // Format axis title.
 chart.getAxisX().getTitle().setShow(true);
 chart.getAxisX().getTitle().getFormat().getFill().solid(Color.yellow);

 // Format legend.
 chart.getLegend().getFormat().getFill().solid(Color.yellow);

 doc.save(getArtifactsDir() + "Charts.ChartFormat.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| color | java.awt.Color |  |

### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| стиль | int |  |
| variant | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| стиль | int |  |
| variant | int |  |

