---
title: "Füllung"
linktitle: "Füllung"
second_title: "Aspose.Words für Java"
description: "Stellt die Füllformatierung für ein Objekt in Java dar."
type: docs
weight: 311
url: /de/java/com.aspose.words/fill/
---

**Inheritance:**
java.lang.Object
```
public class Fill
```

Stellt die Füllformatierung für ein Objekt dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Graphic Elements ][Working with Graphic Elements].

 **Remarks:** 

Verwenden Sie die [ShapeBase.getFill()](../../com.aspose.words/shapebase/\#getFill)- oder die [Font.getFill()](../../com.aspose.words/font/\#getFill)-Eigenschaft, um auf die Füll‑Eigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der [Fill](../../com.aspose.words/fill/)-Klasse direkt.

 **Examples:** 

Zeigt, wie man eine Form mit einer einfarbigen Farbe füllt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBackColor()](#getBackColor) | Liefert ein Color-Objekt, das die Hintergrundfarbe für die Füllung darstellt. |
| [getBackThemeColor()](#getBackThemeColor) | Liefert ein ThemeColor-Objekt, das die Hintergrundfarbe für die Füllung darstellt. |
| [getBackTintAndShade()](#getBackTintAndShade) | Liefert einen double-Wert, der die Hintergrundfarbe aufhellt oder abdunkelt. |
| [getBaseForeColor()](#getBaseForeColor) | Liefert ein Color-Objekt, das die Basis-Vordergrundfarbe für die Füllung ohne Modifikatoren darstellt. |
| [getColor()](#getColor) | Liefert ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |
| [getFillType()](#getFillType) | Liefert einen Fülltyp. |
| [getForeColor()](#getForeColor) | Liefert ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |
| [getForeThemeColor()](#getForeThemeColor) | Liefert ein ThemeColor-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |
| [getForeTintAndShade()](#getForeTintAndShade) | Liefert einen double-Wert, der die Vordergrundfarbe aufhellt oder abdunkelt. |
| [getGradientAngle()](#getGradientAngle) | Liefert den Winkel der Verlauffüllung. |
| [getGradientStops()](#getGradientStops) | Liefert eine Sammlung von [GradientStop](../../com.aspose.words/gradientstop/)-Objekten für die Füllung. |
| [getGradientStyle()](#getGradientStyle) | Liefert den Verlaufstil [GradientStyle](../../com.aspose.words/gradientstyle/) für die Füllung. |
| [getGradientVariant()](#getGradientVariant) | Liefert die Verlaufvariante [GradientVariant](../../com.aspose.words/gradientvariant/) für die Füllung. |
| [getImageBytes()](#getImageBytes) | Liefert die rohen Bytes der Fülltextur oder des Musters. |
| [getOpacity()](#getOpacity) | Liefert den Opazitätsgrad der angegebenen Füllung als Wert zwischen 0.0 (transparent) und 1.0 (undurchsichtig). |
| [getPattern()](#getPattern) | Liefert einen [PatternType](../../com.aspose.words/patterntype/) für die Füllung. |
| [getPresetTexture()](#getPresetTexture) | Liefert eine [PresetTexture](../../com.aspose.words/presettexture/) für die Füllung. |
| [getRotateWithObject()](#getRotateWithObject) | Liefert, ob die Füllung mit dem angegebenen Objekt rotiert. |
| [getTextureAlignment()](#getTextureAlignment) | Liefert die Ausrichtung für die Kacheltextur-Füllung. |
| [getTransparency()](#getTransparency) | Liefert den Transparenzgrad der angegebenen Füllung als Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent). |
| [getVisible()](#getVisible) | Liefert den Wert, der true ist, wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [patterned(int patternType, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Setzt ein Color-Objekt, das die Hintergrundfarbe für die Füllung darstellt. |
| [setBackThemeColor(int value)](#setBackThemeColor-int) | Setzt ein ThemeColor-Objekt, das die Hintergrundfarbe für die Füllung darstellt. |
| [setBackTintAndShade(double value)](#setBackTintAndShade-double) | Setzt einen double-Wert, der die Hintergrundfarbe aufhellt oder abdunkelt. |
| [setColor(Color value)](#setColor-java.awt.Color) | Setzt ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Setzt ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |
| [setForeThemeColor(int value)](#setForeThemeColor-int) | Legt ein ThemeColor-Objekt fest, das die Vordergrundfarbe für die Füllung darstellt. |
| [setForeTintAndShade(double value)](#setForeTintAndShade-double) | Legt einen double-Wert fest, der die Vordergrundfarbe aufhellt oder abdunkelt. |
| [setGradientAngle(double value)](#setGradientAngle-double) | Legt den Winkel der Farbverlauffüllung fest. |
| [setImage(byte[] imageBytes)](#setImage-byte) | Ändert den Fülltyp zu Einzelbild. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Ändert den Fülltyp zu Einzelbild. |
| [setOpacity(double value)](#setOpacity-double) | Legt den Grad der Undurchsichtigkeit der angegebenen Füllung als Wert zwischen 0,0 (klar) und 1,0 (undurchsichtig) fest. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) | Legt fest, ob die Füllung mit dem angegebenen Objekt rotiert. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) | Legt die Ausrichtung für die Kachel-Texturfüllung fest. |
| [setTransparency(double value)](#setTransparency-double) | Legt den Grad der Transparenz der angegebenen Füllung als Wert zwischen 0,0 (undurchsichtig) und 1,0 (klar) fest. |
| [setVisible(boolean value)](#setVisible-boolean) | Setzt den Wert, der true ist, wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |
| [solid()](#solid) | Setzt die Füllung auf eine einheitliche Farbe. |
| [solid(Color color)](#solid-java.awt.Color) | Setzt die Füllung auf eine angegebene einheitliche Farbe. |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int) |  |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Liefert ein Color-Objekt, das die Hintergrundfarbe für die Füllung darstellt.

 **Examples:** 

Zeigt, wie man eine Form mit Farbverläufen füllt.

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
java.awt.Color - Ein Color-Objekt, das die Hintergrundfarbe für die Füllung darstellt.
### getBackThemeColor() {#getBackThemeColor}
```
public int getBackThemeColor()
```


Liefert ein ThemeColor-Objekt, das die Hintergrundfarbe für die Füllung darstellt.

 **Examples:** 

Zeigt, wie man die Themenfarbe für die Vorder-/Hintergrundformfarbe festlegt.

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
int - Ein ThemeColor-Objekt, das die Hintergrundfarbe für die Füllung darstellt. Der zurückgegebene Wert ist einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten.
### getBackTintAndShade() {#getBackTintAndShade}
```
public double getBackTintAndShade()
```


Liefert einen double-Wert, der die Hintergrundfarbe aufhellt oder abdunkelt.

**Returns:**
double - Ein double-Wert, der die Hintergrundfarbe aufhellt oder abdunkelt.
### getBaseForeColor() {#getBaseForeColor}
```
public Color getBaseForeColor()
```


Liefert ein Color-Objekt, das die Basis-Vordergrundfarbe für die Füllung ohne Modifikatoren darstellt.

 **Examples:** 

Zeigt, wie man die Vordergrundfarbe ohne Modifikatoren erhält.

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
java.awt.Color - Ein Color-Objekt, das die Basis-Vordergrundfarbe für die Füllung ohne Modifikatoren darstellt.
### getColor() {#getColor}
```
public Color getColor()
```


Liefert ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt.

 **Remarks:** 

Diese Eigenschaft bewahrt die Alpha-Komponente von java.awt.Color, im Gegensatz zur [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color)-Eigenschaft, die sie auf eine vollständig undurchsichtige Farbe zurücksetzt.

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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
java.awt.Color - Ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt.
### getFillType() {#getFillType}
```
public int getFillType()
```


Liefert einen Fülltyp.

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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
int - Ein Fülltyp. Der zurückgegebene Wert ist einer der [FillType](../../com.aspose.words/filltype/) Konstanten.
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Liefert ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt.

 **Remarks:** 

Diese Eigenschaft setzt die Alpha-Komponente von java.awt.Color auf eine vollständig undurchsichtige Farbe zurück, im Gegensatz zur [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color)-Eigenschaft, die sie bewahrt.

 **Examples:** 

Zeigt, wie man eine Vielzahl von Formen erstellt.

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
java.awt.Color - Ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt.
### getForeThemeColor() {#getForeThemeColor}
```
public int getForeThemeColor()
```


Liefert ein ThemeColor-Objekt, das die Vordergrundfarbe für die Füllung darstellt.

 **Examples:** 

Zeigt, wie man die Themenfarbe für die Vorder-/Hintergrundformfarbe festlegt.

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
int - Ein ThemeColor-Objekt, das die Vordergrundfarbe für die Füllung darstellt. Der zurückgegebene Wert ist einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten.
### getForeTintAndShade() {#getForeTintAndShade}
```
public double getForeTintAndShade()
```


Liefert einen double-Wert, der die Vordergrundfarbe aufhellt oder abdunkelt.

**Returns:**
double - Ein double-Wert, der die Vordergrundfarbe aufhellt oder abdunkelt.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```


Liefert den Winkel der Verlauffüllung.

 **Examples:** 

Zeigt, wie man eine Form mit Farbverläufen füllt.

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
double - Der Winkel der Farbverlauffüllung.
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```


Liefert eine Sammlung von [GradientStop](../../com.aspose.words/gradientstop/)-Objekten für die Füllung.

 **Examples:** 

Zeigt, wie Gradient-Stops zur Farbverlauffüllung hinzugefügt werden.

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


Liefert den Verlaufstil [GradientStyle](../../com.aspose.words/gradientstyle/) für die Füllung.

 **Examples:** 

Zeigt, wie man eine Form mit Farbverläufen füllt.

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
int - Der Gradientstil [GradientStyle](../../com.aspose.words/gradientstyle/) für die Füllung. Der zurückgegebene Wert ist einer der [GradientStyle](../../com.aspose.words/gradientstyle/) Konstanten.
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```


Liefert die Verlaufvariante [GradientVariant](../../com.aspose.words/gradientvariant/) für die Füllung.

 **Examples:** 

Zeigt, wie man eine Form mit Farbverläufen füllt.

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
int - Die Gradientvariante [GradientVariant](../../com.aspose.words/gradientvariant/) für die Füllung. Der zurückgegebene Wert ist einer der [GradientVariant](../../com.aspose.words/gradientvariant/) Konstanten.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Liefert die rohen Bytes der Fülltextur oder des Musters.

 **Remarks:** 

Der Standardwert ist  null .

 **Examples:** 

Zeigt, wie man eine Vielzahl von Formen erstellt.

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
byte[] - Die Rohbytes der Fülltextur oder des Musters.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


Liefert den Opazitätsgrad der angegebenen Füllung als Wert zwischen 0.0 (transparent) und 1.0 (undurchsichtig).

 **Remarks:** 

Diese Eigenschaft ist das Gegenstück zur Eigenschaft [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Zeigt, wie man eine Form mit einer einfarbigen Farbe füllt.

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
double - Der Grad der Undurchsichtigkeit der angegebenen Füllung als Wert zwischen 0.0 (klar) und 1.0 (undurchsichtig).
### getPattern() {#getPattern}
```
public int getPattern()
```


Liefert einen [PatternType](../../com.aspose.words/patterntype/) für die Füllung.

 **Examples:** 

Zeigt, wie man ein Muster für eine Form festlegt.

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
int - Ein [PatternType](../../com.aspose.words/patterntype/) für die Füllung. Der zurückgegebene Wert ist einer der [PatternType](../../com.aspose.words/patterntype/) Konstanten.
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```


Liefert eine [PresetTexture](../../com.aspose.words/presettexture/) für die Füllung.

 **Examples:** 

Zeigt, wie die Textur innerhalb der Form gefüllt und gekachelt wird.

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
int - Eine [PresetTexture](../../com.aspose.words/presettexture/) für die Füllung. Der zurückgegebene Wert ist einer der [PresetTexture](../../com.aspose.words/presettexture/) Konstanten.
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```


Liefert, ob die Füllung mit dem angegebenen Objekt rotiert.

**Returns:**
boolean - Ob die Füllung mit dem angegebenen Objekt rotiert.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```


Liefert die Ausrichtung für die Kacheltextur-Füllung.

 **Examples:** 

Zeigt, wie die Textur innerhalb der Form gefüllt und gekachelt wird.

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
int - Die Ausrichtung für die Kacheltexturfüllung. Der zurückgegebene Wert ist einer der [TextureAlignment](../../com.aspose.words/texturealignment/) Konstanten.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Liefert den Transparenzgrad der angegebenen Füllung als Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent).

 **Remarks:** 

Diese Eigenschaft ist das Gegenstück zur Eigenschaft [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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
double - Der Grad der Transparenz der angegebenen Füllung als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Liefert den Wert, der true ist, wenn die auf diese Instanz angewendete Formatierung sichtbar ist.

 **Examples:** 

Zeigt, wie man eine Vielzahl von Formen erstellt.

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
boolean - Wert, der true ist, wenn die auf diese Instanz angewendete Formatierung sichtbar ist.
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Stil | int |  |
| Variante | int |  |
| Grad | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Farbe | java.awt.Color |  |
| Stil | int |  |
| Variante | int |  |
| Grad | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| MusterTyp | int |  |

### patterned(int patternType, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color}
```
public void patterned(int patternType, Color foreColor, Color backColor)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| MusterTyp | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| VoreingestellteTextur | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Setzt ein Color-Objekt, das die Hintergrundfarbe für die Füllung darstellt.

 **Examples:** 

Zeigt, wie man eine Form mit Farbverläufen füllt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Ein Color-Objekt, das die Hintergrundfarbe für die Füllung darstellt. |

### setBackThemeColor(int value) {#setBackThemeColor-int}
```
public void setBackThemeColor(int value)
```


Setzt ein ThemeColor-Objekt, das die Hintergrundfarbe für die Füllung darstellt.

 **Examples:** 

Zeigt, wie man die Themenfarbe für die Vorder-/Hintergrundformfarbe festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein ThemeColor-Objekt, das die Hintergrundfarbe für die Füllung darstellt. Der Wert muss einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten sein. |

### setBackTintAndShade(double value) {#setBackTintAndShade-double}
```
public void setBackTintAndShade(double value)
```


Setzt einen double-Wert, der die Hintergrundfarbe aufhellt oder abdunkelt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der die Hintergrundfarbe aufhellt oder abdunkelt. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Setzt ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt.

 **Remarks:** 

Diese Eigenschaft bewahrt die Alpha-Komponente von java.awt.Color, im Gegensatz zur [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color)-Eigenschaft, die sie auf eine vollständig undurchsichtige Farbe zurücksetzt.

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Setzt ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt.

 **Remarks:** 

Diese Eigenschaft setzt die Alpha-Komponente von java.awt.Color auf eine vollständig undurchsichtige Farbe zurück, im Gegensatz zur [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color)-Eigenschaft, die sie bewahrt.

 **Examples:** 

Zeigt, wie man eine Vielzahl von Formen erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Ein Color-Objekt, das die Vordergrundfarbe für die Füllung darstellt. |

### setForeThemeColor(int value) {#setForeThemeColor-int}
```
public void setForeThemeColor(int value)
```


Legt ein ThemeColor-Objekt fest, das die Vordergrundfarbe für die Füllung darstellt.

 **Examples:** 

Zeigt, wie man die Themenfarbe für die Vorder-/Hintergrundformfarbe festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein ThemeColor-Objekt, das die Vordergrundfarbe für die Füllung darstellt. Der Wert muss einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten sein. |

### setForeTintAndShade(double value) {#setForeTintAndShade-double}
```
public void setForeTintAndShade(double value)
```


Legt einen double-Wert fest, der die Vordergrundfarbe aufhellt oder abdunkelt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der die Vordergrundfarbe aufhellt oder abdunkelt. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```


Legt den Winkel der Farbverlauffüllung fest.

 **Examples:** 

Zeigt, wie man eine Form mit Farbverläufen füllt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Winkel der Gradientfüllung. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```


Ändert den Fülltyp zu Einzelbild.

 **Examples:** 

Zeigt, wie man den Fülltyp einer Form als Bild festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| BildBytes | byte[] | Das Bild-Byte-Array. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Ändert den Fülltyp zu Einzelbild.

 **Examples:** 

Zeigt, wie man den Fülltyp einer Form als Bild festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Der Pfad zur Bilddatei. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


Legt den Grad der Undurchsichtigkeit der angegebenen Füllung als Wert zwischen 0,0 (klar) und 1,0 (undurchsichtig) fest.

 **Remarks:** 

Diese Eigenschaft ist das Gegenstück zur Eigenschaft [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Zeigt, wie man eine Form mit einer einfarbigen Farbe füllt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Grad der Undurchsichtigkeit der angegebenen Füllung als Wert zwischen 0.0 (klar) und 1.0 (undurchsichtig). |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```


Legt fest, ob die Füllung mit dem angegebenen Objekt rotiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob die Füllung mit dem angegebenen Objekt rotiert. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```


Legt die Ausrichtung für die Kachel-Texturfüllung fest.

 **Examples:** 

Zeigt, wie die Textur innerhalb der Form gefüllt und gekachelt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Ausrichtung für Kachel-Texturfüllung. Der Wert muss einer der Konstanten von [TextureAlignment](../../com.aspose.words/texturealignment/) sein. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Legt den Grad der Transparenz der angegebenen Füllung als Wert zwischen 0,0 (undurchsichtig) und 1,0 (klar) fest.

 **Remarks:** 

Diese Eigenschaft ist das Gegenstück zur Eigenschaft [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Grad der Transparenz der angegebenen Füllung als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar). |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


Setzt den Wert, der true ist, wenn die auf diese Instanz angewendete Formatierung sichtbar ist.

 **Examples:** 

Zeigt, wie man eine Vielzahl von Formen erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Wert, der true ist, wenn die auf diese Instanz angewandte Formatierung sichtbar ist. |

### solid() {#solid}
```
public void solid()
```


Setzt die Füllung auf eine einheitliche Farbe.

 **Remarks:** 

Verwenden Sie diese Methode, um beliebige Füllungen wieder in eine Vollfarbe umzuwandeln.

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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


Setzt die Füllung auf eine angegebene einheitliche Farbe.

 **Remarks:** 

Verwenden Sie diese Methode, um beliebige Füllungen wieder in eine Vollfarbe umzuwandeln.

 **Examples:** 

Zeigt, wie die Diagrammformatierung verwendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Farbe | java.awt.Color |  |

### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Stil | int |  |
| Variante | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| Stil | int |  |
| Variante | int |  |

