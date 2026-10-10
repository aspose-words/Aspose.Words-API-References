---
title: "ملء"
linktitle: "ملء"
second_title: "Aspose.Words لـ Java"
description: "يمثل تنسيق الملء لكائن في Java."
type: docs
weight: 311
url: /ar/java/com.aspose.words/fill/
---

**Inheritance:**
java.lang.Object
```
public class Fill
```

يمثل تنسيق التعبئة لكائن.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Graphic Elements ][Working with Graphic Elements].

 **Remarks:** 

استخدم خاصية [ShapeBase.getFill()](../../com.aspose.words/shapebase/\#getFill) أو [Font.getFill()](../../com.aspose.words/font/\#getFill) للوصول إلى خصائص الملء لكائن. لا تقوم بإنشاء مثيلات من الفئة [Fill](../../com.aspose.words/fill/) مباشرةً.

 **Examples:** 

يوضح كيفية ملء شكل بلون صلب.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBackColor()](#getBackColor) | يحصل على كائن Color يمثل لون الخلفية للملء. |
| [getBackThemeColor()](#getBackThemeColor) | يحصل على كائن ThemeColor يمثل لون الخلفية للملء. |
| [getBackTintAndShade()](#getBackTintAndShade) | يحصل على قيمة مزدوجة تُفتح أو تُغميق لون الخلفية. |
| [getBaseForeColor()](#getBaseForeColor) | يحصل على كائن Color يمثل لون المقدمة الأساسي للملء دون أي تعديلات. |
| [getColor()](#getColor) | يحصل على كائن Color يمثل لون المقدمة للملء. |
| [getFillType()](#getFillType) | يحصل على نوع الملء. |
| [getForeColor()](#getForeColor) | يحصل على كائن Color يمثل لون المقدمة للملء. |
| [getForeThemeColor()](#getForeThemeColor) | يحصل على كائن ThemeColor يمثل لون المقدمة للملء. |
| [getForeTintAndShade()](#getForeTintAndShade) | يحصل على قيمة مزدوجة تُفتح أو تُغميق لون المقدمة. |
| [getGradientAngle()](#getGradientAngle) | يحصل على زاوية التدرج للملء. |
| [getGradientStops()](#getGradientStops) | يحصل على مجموعة من كائنات [GradientStop](../../com.aspose.words/gradientstop/) للملء. |
| [getGradientStyle()](#getGradientStyle) | يحصل على نمط التدرج [GradientStyle](../../com.aspose.words/gradientstyle/) للملء. |
| [getGradientVariant()](#getGradientVariant) | يحصل على متغير التدرج [GradientVariant](../../com.aspose.words/gradientvariant/) للملء. |
| [getImageBytes()](#getImageBytes) | يحصل على البايتات الخام لنسيج أو نمط التعبئة. |
| [getOpacity()](#getOpacity) | يحصل على درجة العتامة للتعبئة المحددة كقيمة بين 0.0 (شفافة) و 1.0 (معتمة). |
| [getPattern()](#getPattern) | يحصل على [PatternType](../../com.aspose.words/patterntype/) للتعبئة. |
| [getPresetTexture()](#getPresetTexture) | يحصل على [PresetTexture](../../com.aspose.words/presettexture/) للتعبئة. |
| [getRotateWithObject()](#getRotateWithObject) | يحصل على ما إذا كانت التعبئة تدور مع الكائن المحدد. |
| [getTextureAlignment()](#getTextureAlignment) | يحصل على المحاذاة لتعبئة نسيج البلاط. |
| [getTransparency()](#getTransparency) | يحصل على درجة الشفافية للتعبئة المحددة كقيمة بين 0.0 (معتمة) و 1.0 (شفافة). |
| [getVisible()](#getVisible) | يحصل على القيمة التي تكون  true  إذا كان التنسيق المطبق على هذه الحالة مرئياً. |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [patterned(int patternType, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | يضبط كائن Color الذي يمثل لون الخلفية للتعبئة. |
| [setBackThemeColor(int value)](#setBackThemeColor-int) | يضبط كائن ThemeColor الذي يمثل لون الخلفية للتعبئة. |
| [setBackTintAndShade(double value)](#setBackTintAndShade-double) | يضبط قيمة مزدوجة تُفتح أو تُغميق لون الخلفية. |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط كائن Color الذي يمثل لون المقدمة للتعبئة. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | يضبط كائن Color الذي يمثل لون المقدمة للتعبئة. |
| [setForeThemeColor(int value)](#setForeThemeColor-int) | يضبط كائن ThemeColor الذي يمثل لون المقدمة للتعبئة. |
| [setForeTintAndShade(double value)](#setForeTintAndShade-double) | يضبط قيمة مزدوجة تُفتح أو تُغميق لون المقدمة. |
| [setGradientAngle(double value)](#setGradientAngle-double) | يضبط زاوية تعبئة التدرج. |
| [setImage(byte[] imageBytes)](#setImage-byte) | يغيّر نوع التعبئة إلى صورة واحدة. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | يغيّر نوع التعبئة إلى صورة واحدة. |
| [setOpacity(double value)](#setOpacity-double) | يضبط درجة العتامة للتعبئة المحددة كقيمة بين 0.0 (شفافة) و 1.0 (معتمة). |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) | يضبط ما إذا كانت التعبئة تدور مع الكائن المحدد. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) | يضبط المحاذاة لتعبئة نسيج البلاط. |
| [setTransparency(double value)](#setTransparency-double) | يضبط درجة الشفافية للتعبئة المحددة كقيمة بين 0.0 (معتمة) و 1.0 (شفافة). |
| [setVisible(boolean value)](#setVisible-boolean) | يضبط القيمة التي تكون  true  إذا كان التنسيق المطبق على هذه الحالة مرئياً. |
| [solid()](#solid) | يضبط التعبئة إلى لون موحد. |
| [solid(Color color)](#solid-java.awt.Color) | يضبط التعبئة إلى لون موحد محدد. |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int) |  |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


يحصل على كائن Color يمثل لون الخلفية للملء.

 **Examples:** 

يعرض كيفية ملء شكل بتدرجات.

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
java.awt.Color - كائن Color يمثل لون الخلفية للتعبئة.
### getBackThemeColor() {#getBackThemeColor}
```
public int getBackThemeColor()
```


يحصل على كائن ThemeColor يمثل لون الخلفية للملء.

 **Examples:** 

يعرض كيفية تعيين لون السمة للون الشكل الأمامي/الخلفي.

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
int - كائن ThemeColor يمثل لون الخلفية للتعبئة. القيمة المرجعة هي واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/).
### getBackTintAndShade() {#getBackTintAndShade}
```
public double getBackTintAndShade()
```


يحصل على قيمة مزدوجة تُفتح أو تُغميق لون الخلفية.

**Returns:**
double - قيمة مزدوجة تُفتح أو تُغمق لون الخلفية.
### getBaseForeColor() {#getBaseForeColor}
```
public Color getBaseForeColor()
```


يحصل على كائن Color يمثل لون المقدمة الأساسي للملء دون أي تعديلات.

 **Examples:** 

يعرض كيفية الحصول على لون المقدمة بدون معدلات.

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
java.awt.Color - كائن Color يمثل لون المقدمة الأساسي للتعبئة بدون أي معدلات.
### getColor() {#getColor}
```
public Color getColor()
```


يحصل على كائن Color يمثل لون المقدمة للملء.

 **Remarks:** 

هذه الخاصية تحتفظ بالمكوّن ألفا من java.awt.Color، على عكس خاصية [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color) التي تعيد تعيينه إلى لون غير شفاف بالكامل.

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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
java.awt.Color - كائن Color يمثل لون المقدمة للتعبئة.
### getFillType() {#getFillType}
```
public int getFillType()
```


يحصل على نوع الملء.

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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
int - نوع تعبئة. القيمة المرجعة هي واحدة من ثوابت [FillType](../../com.aspose.words/filltype/).
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


يحصل على كائن Color يمثل لون المقدمة للملء.

 **Remarks:** 

هذه الخاصية تعيد تعيين المكوّن ألفا من java.awt.Color إلى لون غير شفاف بالكامل على عكس خاصية [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) التي تحتفظ به.

 **Examples:** 

يعرض لإنشاء مجموعة متنوعة من الأشكال.

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
java.awt.Color - كائن Color يمثل لون المقدمة للتعبئة.
### getForeThemeColor() {#getForeThemeColor}
```
public int getForeThemeColor()
```


يحصل على كائن ThemeColor يمثل لون المقدمة للملء.

 **Examples:** 

يعرض كيفية تعيين لون السمة للون الشكل الأمامي/الخلفي.

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
int - كائن ThemeColor يمثل لون المقدمة للتعبئة. القيمة المرجعة هي واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/).
### getForeTintAndShade() {#getForeTintAndShade}
```
public double getForeTintAndShade()
```


يحصل على قيمة مزدوجة تُفتح أو تُغميق لون المقدمة.

**Returns:**
double - قيمة مزدوجة تُفتح أو تُغمق لون المقدمة.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```


يحصل على زاوية التدرج للملء.

 **Examples:** 

يعرض كيفية ملء شكل بتدرجات.

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
double - زاوية التعبئة المتدرجة.
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```


يحصل على مجموعة من كائنات [GradientStop](../../com.aspose.words/gradientstop/) للملء.

 **Examples:** 

يظهر كيفية إضافة نقاط التدرج إلى تعبئة التدرج.

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


يحصل على نمط التدرج [GradientStyle](../../com.aspose.words/gradientstyle/) للملء.

 **Examples:** 

يعرض كيفية ملء شكل بتدرجات.

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
int - نمط التدرج [GradientStyle](../../com.aspose.words/gradientstyle/) للتعبئة. القيمة المرجعة هي واحدة من ثوابت [GradientStyle](../../com.aspose.words/gradientstyle/).
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```


يحصل على متغير التدرج [GradientVariant](../../com.aspose.words/gradientvariant/) للملء.

 **Examples:** 

يعرض كيفية ملء شكل بتدرجات.

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
int - متغيّر التدرج [GradientVariant](../../com.aspose.words/gradientvariant/) للتعبئة. القيمة المرجعة هي واحدة من ثوابت [GradientVariant](../../com.aspose.words/gradientvariant/).
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


يحصل على البايتات الخام لنسيج أو نمط التعبئة.

 **Remarks:** 

القيمة الافتراضية هي  null .

 **Examples:** 

يعرض لإنشاء مجموعة متنوعة من الأشكال.

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
byte[] - البايتات الخام لنسيج أو نمط التعبئة.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


يحصل على درجة العتامة للتعبئة المحددة كقيمة بين 0.0 (شفافة) و 1.0 (معتمة).

 **Remarks:** 

هذه الخاصية هي عكس الخاصية [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

يوضح كيفية ملء شكل بلون صلب.

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
double - درجة العتمة للتعبئة المحددة كقيمة بين 0.0 (شفافة) و 1.0 (معتمة).
### getPattern() {#getPattern}
```
public int getPattern()
```


يحصل على [PatternType](../../com.aspose.words/patterntype/) للتعبئة.

 **Examples:** 

يعرض كيفية تعيين نمط لشكل.

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
int - [PatternType](../../com.aspose.words/patterntype/) للتعبئة. القيمة المرجعة هي واحدة من ثوابت [PatternType](../../com.aspose.words/patterntype/).
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```


يحصل على [PresetTexture](../../com.aspose.words/presettexture/) للتعبئة.

 **Examples:** 

يظهر كيفية تعبئة وتكرار النسيج داخل الشكل.

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
int - [PresetTexture](../../com.aspose.words/presettexture/) للتعبئة. القيمة المرجعة هي واحدة من ثوابت [PresetTexture](../../com.aspose.words/presettexture/).
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```


يحصل على ما إذا كانت التعبئة تدور مع الكائن المحدد.

**Returns:**
boolean - ما إذا كانت التعبئة تدور مع الكائن المحدد.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```


يحصل على المحاذاة لتعبئة نسيج البلاط.

 **Examples:** 

يظهر كيفية تعبئة وتكرار النسيج داخل الشكل.

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
int - محاذاة تعبئة نسيج البلاط. القيمة المرجعة هي واحدة من ثوابت [TextureAlignment](../../com.aspose.words/texturealignment/).
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


يحصل على درجة الشفافية للتعبئة المحددة كقيمة بين 0.0 (معتمة) و 1.0 (شفافة).

 **Remarks:** 

هذه الخاصية هي عكس الخاصية [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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
double - درجة الشفافية للملء المحدد كقيمة بين 0.0 (معتم) و 1.0 (شفاف).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


يحصل على القيمة التي تكون  true  إذا كان التنسيق المطبق على هذه الحالة مرئياً.

 **Examples:** 

يعرض لإنشاء مجموعة متنوعة من الأشكال.

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
boolean - القيمة التي تكون  true  إذا كان التنسيق المطبق على هذه الحالة مرئيًا.
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| النمط | int |  |
| variant | int |  |
| degree | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| لون | java.awt.Color |  |
| النمط | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| patternType | int |  |

### patterned(int patternType, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color}
```
public void patterned(int patternType, Color foreColor, Color backColor)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| patternType | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| presetTexture | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


يضبط كائن Color الذي يمثل لون الخلفية للتعبئة.

 **Examples:** 

يعرض كيفية ملء شكل بتدرجات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | كائن Color يمثل لون الخلفية للملء. |

### setBackThemeColor(int value) {#setBackThemeColor-int}
```
public void setBackThemeColor(int value)
```


يضبط كائن ThemeColor الذي يمثل لون الخلفية للتعبئة.

 **Examples:** 

يعرض كيفية تعيين لون السمة للون الشكل الأمامي/الخلفي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | كائن ThemeColor يمثل لون الخلفية للملء. يجب أن تكون القيمة واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setBackTintAndShade(double value) {#setBackTintAndShade-double}
```
public void setBackTintAndShade(double value)
```


يضبط قيمة مزدوجة تُفتح أو تُغميق لون الخلفية.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة double التي تُفتح أو تُغمق لون الخلفية. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


يضبط كائن Color الذي يمثل لون المقدمة للتعبئة.

 **Remarks:** 

هذه الخاصية تحتفظ بالمكوّن ألفا من java.awt.Color، على عكس خاصية [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color) التي تعيد تعيينه إلى لون غير شفاف بالكامل.

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | كائن Color يمثل لون المقدمة للملء. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


يضبط كائن Color الذي يمثل لون المقدمة للتعبئة.

 **Remarks:** 

هذه الخاصية تعيد تعيين المكوّن ألفا من java.awt.Color إلى لون غير شفاف بالكامل على عكس خاصية [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) التي تحتفظ به.

 **Examples:** 

يعرض لإنشاء مجموعة متنوعة من الأشكال.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | كائن Color يمثل لون المقدمة للملء. |

### setForeThemeColor(int value) {#setForeThemeColor-int}
```
public void setForeThemeColor(int value)
```


يضبط كائن ThemeColor الذي يمثل لون المقدمة للتعبئة.

 **Examples:** 

يعرض كيفية تعيين لون السمة للون الشكل الأمامي/الخلفي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | كائن ThemeColor يمثل لون المقدمة للملء. يجب أن تكون القيمة واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setForeTintAndShade(double value) {#setForeTintAndShade-double}
```
public void setForeTintAndShade(double value)
```


يضبط قيمة مزدوجة تُفتح أو تُغميق لون المقدمة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة double التي تُفتح أو تُغمق لون المقدمة. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```


يضبط زاوية تعبئة التدرج.

 **Examples:** 

يعرض كيفية ملء شكل بتدرجات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | زاوية الملء المتدرج. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```


يغيّر نوع التعبئة إلى صورة واحدة.

 **Examples:** 

يوضح كيفية تعيين نوع ملء الشكل كصورة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBytes | byte[] | مصفوفة بايتات الصورة. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


يغيّر نوع التعبئة إلى صورة واحدة.

 **Examples:** 

يوضح كيفية تعيين نوع ملء الشكل كصورة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | المسار إلى ملف الصورة. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


يضبط درجة العتامة للتعبئة المحددة كقيمة بين 0.0 (شفافة) و 1.0 (معتمة).

 **Remarks:** 

هذه الخاصية هي عكس الخاصية [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

يوضح كيفية ملء شكل بلون صلب.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | درجة التعتيم للملء المحدد كقيمة بين 0.0 (شفاف) و 1.0 (معتم). |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```


يضبط ما إذا كانت التعبئة تدور مع الكائن المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان الملء يدور مع الكائن المحدد. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```


يضبط المحاذاة لتعبئة نسيج البلاط.

 **Examples:** 

يظهر كيفية تعبئة وتكرار النسيج داخل الشكل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | محاذاة ملء نسيج البلاط. يجب أن تكون القيمة واحدة من ثوابت [TextureAlignment](../../com.aspose.words/texturealignment/) constants. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


يضبط درجة الشفافية للتعبئة المحددة كقيمة بين 0.0 (معتمة) و 1.0 (شفافة).

 **Remarks:** 

هذه الخاصية هي عكس الخاصية [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | درجة الشفافية للملء المحدد كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


يضبط القيمة التي تكون  true  إذا كان التنسيق المطبق على هذه الحالة مرئياً.

 **Examples:** 

يعرض لإنشاء مجموعة متنوعة من الأشكال.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة التي تكون  true  إذا كان التنسيق المطبق على هذه الحالة مرئيًا. |

### solid() {#solid}
```
public void solid()
```


يضبط التعبئة إلى لون موحد.

 **Remarks:** 

استخدم هذه الطريقة لتحويل أي من الملئات إلى ملء صلب.

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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


يضبط التعبئة إلى لون موحد محدد.

 **Remarks:** 

استخدم هذه الطريقة لتحويل أي من الملئات إلى ملء صلب.

 **Examples:** 

يوضح كيفية استخدام تنسيق المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| لون | java.awt.Color |  |

### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| النمط | int |  |
| variant | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| النمط | int |  |
| variant | int |  |

