---
title: "Remplissage"
linktitle: "Remplissage"
second_title: "Aspose.Words pour Java"
description: "Représente le format de remplissage d'un objet en Java."
type: docs
weight: 311
url: /fr/java/com.aspose.words/fill/
---

**Inheritance:**
java.lang.Object
```
public class Fill
```

Représente le format de remplissage d'un objet.

Pour en savoir plus, consultez l'article de documentation [ Working with Graphic Elements ][Working with Graphic Elements].

 **Remarks:** 

Utilisez la propriété [ShapeBase.getFill()](../../com.aspose.words/shapebase/\#getFill) ou [Font.getFill()](../../com.aspose.words/font/\#getFill) pour accéder aux propriétés de remplissage d'un objet. Vous ne créez pas d'instances de la classe [Fill](../../com.aspose.words/fill/) directement.

 **Examples:** 

Montre comment remplir une forme avec une couleur unie.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBackColor()](#getBackColor) | Obtient un objet Color qui représente la couleur d'arrière-plan du remplissage. |
| [getBackThemeColor()](#getBackThemeColor) | Obtient un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage. |
| [getBackTintAndShade()](#getBackTintAndShade) | Obtient une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan. |
| [getBaseForeColor()](#getBaseForeColor) | Obtient un objet Color qui représente la couleur de premier plan de base du remplissage sans aucun modificateur. |
| [getColor()](#getColor) | Obtient un objet Color qui représente la couleur de premier plan du remplissage. |
| [getFillType()](#getFillType) | Obtient un type de remplissage. |
| [getForeColor()](#getForeColor) | Obtient un objet Color qui représente la couleur de premier plan du remplissage. |
| [getForeThemeColor()](#getForeThemeColor) | Obtient un objet ThemeColor qui représente la couleur de premier plan du remplissage. |
| [getForeTintAndShade()](#getForeTintAndShade) | Obtient une valeur double qui éclaircit ou assombrit la couleur de premier plan. |
| [getGradientAngle()](#getGradientAngle) | Obtient l'angle du remplissage en dégradé. |
| [getGradientStops()](#getGradientStops) | Obtient une collection d'objets [GradientStop](../../com.aspose.words/gradientstop/) pour le remplissage. |
| [getGradientStyle()](#getGradientStyle) | Obtient le style de dégradé [GradientStyle](../../com.aspose.words/gradientstyle/) pour le remplissage. |
| [getGradientVariant()](#getGradientVariant) | Obtient la variante de dégradé [GradientVariant](../../com.aspose.words/gradientvariant/) pour le remplissage. |
| [getImageBytes()](#getImageBytes) | Obtient les octets bruts de la texture ou du motif de remplissage. |
| [getOpacity()](#getOpacity) | Obtient le degré d'opacité du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (transparent) et 1.0 (opaque). |
| [getPattern()](#getPattern) | Obtient un [PatternType](../../com.aspose.words/patterntype/) pour le remplissage. |
| [getPresetTexture()](#getPresetTexture) | Obtient une [PresetTexture](../../com.aspose.words/presettexture/) pour le remplissage. |
| [getRotateWithObject()](#getRotateWithObject) | Obtient si le remplissage tourne avec l'objet spécifié. |
| [getTextureAlignment()](#getTextureAlignment) | Obtient l'alignement pour le remplissage de texture en mosaïque. |
| [getTransparency()](#getTransparency) | Obtient le degré de transparence du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). |
| [getVisible()](#getVisible) | Obtient la valeur qui est  true  si le formatage appliqué à cette instance est visible. |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [patterned(int patternType, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Définit un objet Color qui représente la couleur d'arrière-plan du remplissage. |
| [setBackThemeColor(int value)](#setBackThemeColor-int) | Définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage. |
| [setBackTintAndShade(double value)](#setBackTintAndShade-double) | Définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan. |
| [setColor(Color value)](#setColor-java.awt.Color) | Définit un objet Color qui représente la couleur de premier plan du remplissage. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Définit un objet Color qui représente la couleur de premier plan du remplissage. |
| [setForeThemeColor(int value)](#setForeThemeColor-int) | Définit un objet ThemeColor qui représente la couleur de premier plan du remplissage. |
| [setForeTintAndShade(double value)](#setForeTintAndShade-double) | Définit une valeur double qui éclaircit ou assombrit la couleur de premier plan. |
| [setGradientAngle(double value)](#setGradientAngle-double) | Définit l'angle du remplissage en dégradé. |
| [setImage(byte[] imageBytes)](#setImage-byte) | Modifie le type de remplissage en image unique. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Modifie le type de remplissage en image unique. |
| [setOpacity(double value)](#setOpacity-double) | Définit le degré d'opacité du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (transparent) et 1.0 (opaque). |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) | Définit si le remplissage tourne avec l'objet spécifié. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) | Définit l'alignement pour le remplissage de texture en mosaïque. |
| [setTransparency(double value)](#setTransparency-double) | Définit le degré de transparence du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). |
| [setVisible(boolean value)](#setVisible-boolean) | Définit la valeur qui est  true  si le formatage appliqué à cette instance est visible. |
| [solid()](#solid) | Définit le remplissage à une couleur uniforme. |
| [solid(Color color)](#solid-java.awt.Color) | Définit le remplissage à une couleur uniforme spécifiée. |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int) |  |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Obtient un objet Color qui représente la couleur d'arrière-plan du remplissage.

 **Examples:** 

Montre comment remplir une forme avec des dégradés.

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
java.awt.Color - Un objet Color qui représente la couleur d'arrière-plan du remplissage.
### getBackThemeColor() {#getBackThemeColor}
```
public int getBackThemeColor()
```


Obtient un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage.

 **Examples:** 

Montre comment définir la couleur de thème pour la couleur de forme avant-plan/arrière-plan.

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
int - Un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage. La valeur renvoyée est l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getBackTintAndShade() {#getBackTintAndShade}
```
public double getBackTintAndShade()
```


Obtient une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan.

**Returns:**
double - Une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan.
### getBaseForeColor() {#getBaseForeColor}
```
public Color getBaseForeColor()
```


Obtient un objet Color qui représente la couleur de premier plan de base du remplissage sans aucun modificateur.

 **Examples:** 

Montre comment obtenir la couleur avant-plan sans modificateurs.

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
java.awt.Color - Un objet Color qui représente la couleur de base avant-plan du remplissage sans aucun modificateur.
### getColor() {#getColor}
```
public Color getColor()
```


Obtient un objet Color qui représente la couleur de premier plan du remplissage.

 **Remarks:** 

Cette propriété préserve le composant alpha du java.awt.Color, contrairement à la propriété [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color), qui le réinitialise à une couleur totalement opaque.

 **Examples:** 

Montre comment convertir n'importe quel remplissage en remplissage uni.

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
java.awt.Color - Un objet Color qui représente la couleur avant-plan du remplissage.
### getFillType() {#getFillType}
```
public int getFillType()
```


Obtient un type de remplissage.

 **Examples:** 

Montre comment convertir n'importe quel remplissage en remplissage uni.

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
int - Un type de remplissage. La valeur renvoyée est l'une des constantes [FillType](../../com.aspose.words/filltype/).
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Obtient un objet Color qui représente la couleur de premier plan du remplissage.

 **Remarks:** 

Cette propriété réinitialise le composant alpha du java.awt.Color à une couleur totalement opaque, contrairement à la propriété [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color), qui le préserve.

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

**Returns:**
java.awt.Color - Un objet Color qui représente la couleur avant-plan du remplissage.
### getForeThemeColor() {#getForeThemeColor}
```
public int getForeThemeColor()
```


Obtient un objet ThemeColor qui représente la couleur de premier plan du remplissage.

 **Examples:** 

Montre comment définir la couleur de thème pour la couleur de forme avant-plan/arrière-plan.

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
int - Un objet ThemeColor qui représente la couleur avant-plan du remplissage. La valeur renvoyée est l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getForeTintAndShade() {#getForeTintAndShade}
```
public double getForeTintAndShade()
```


Obtient une valeur double qui éclaircit ou assombrit la couleur de premier plan.

**Returns:**
double - Une valeur double qui éclaircit ou assombrit la couleur avant-plan.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```


Obtient l'angle du remplissage en dégradé.

 **Examples:** 

Montre comment remplir une forme avec des dégradés.

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
double - L'angle du remplissage en dégradé.
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```


Obtient une collection d'objets [GradientStop](../../com.aspose.words/gradientstop/) pour le remplissage.

 **Examples:** 

Montre comment ajouter des points d'arrêt de dégradé au remplissage en dégradé.

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


Obtient le style de dégradé [GradientStyle](../../com.aspose.words/gradientstyle/) pour le remplissage.

 **Examples:** 

Montre comment remplir une forme avec des dégradés.

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
int - Le style de dégradé [GradientStyle](../../com.aspose.words/gradientstyle/) du remplissage. La valeur renvoyée est l'une des constantes [GradientStyle](../../com.aspose.words/gradientstyle/).
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```


Obtient la variante de dégradé [GradientVariant](../../com.aspose.words/gradientvariant/) pour le remplissage.

 **Examples:** 

Montre comment remplir une forme avec des dégradés.

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
int - La variante de dégradé [GradientVariant](../../com.aspose.words/gradientvariant/) du remplissage. La valeur renvoyée est l'une des constantes [GradientVariant](../../com.aspose.words/gradientvariant/).
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Obtient les octets bruts de la texture ou du motif de remplissage.

 **Remarks:** 

La valeur par défaut est  null .

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

**Returns:**
byte[] - Les octets bruts de la texture ou du motif du remplissage.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


Obtient le degré d'opacité du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (transparent) et 1.0 (opaque).

 **Remarks:** 

Cette propriété est l'opposée de la propriété [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Montre comment remplir une forme avec une couleur unie.

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
double - Le degré d'opacité du remplissage spécifié, exprimé par une valeur entre 0.0 (transparent) et 1.0 (opaque).
### getPattern() {#getPattern}
```
public int getPattern()
```


Obtient un [PatternType](../../com.aspose.words/patterntype/) pour le remplissage.

 **Examples:** 

Montre comment définir un motif pour une forme.

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
int - Un [PatternType](../../com.aspose.words/patterntype/) pour le remplissage. La valeur renvoyée est l'une des constantes [PatternType](../../com.aspose.words/patterntype/).
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```


Obtient une [PresetTexture](../../com.aspose.words/presettexture/) pour le remplissage.

 **Examples:** 

Montre comment remplir et carreliser la texture à l'intérieur de la forme.

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
int - Un [PresetTexture](../../com.aspose.words/presettexture/) pour le remplissage. La valeur renvoyée est l'une des constantes [PresetTexture](../../com.aspose.words/presettexture/).
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```


Obtient si le remplissage tourne avec l'objet spécifié.

**Returns:**
boolean - Indique si le remplissage tourne avec l'objet spécifié.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```


Obtient l'alignement pour le remplissage de texture en mosaïque.

 **Examples:** 

Montre comment remplir et carreliser la texture à l'intérieur de la forme.

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
int - L'alignement du remplissage de texture en mosaïque. La valeur renvoyée est l'une des constantes [TextureAlignment](../../com.aspose.words/texturealignment/).
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Obtient le degré de transparence du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (opaque) et 1.0 (transparent).

 **Remarks:** 

Cette propriété est l'opposée de la propriété [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Montre comment convertir n'importe quel remplissage en remplissage uni.

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
double - Le degré de transparence du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (opaque) et 1.0 (transparent).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Obtient la valeur qui est  true  si le formatage appliqué à cette instance est visible.

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

**Returns:**
boolean - Valeur qui est  true  si le formatage appliqué à cette instance est visible.
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| couleur | java.awt.Color |  |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| patternType | int |  |

### patterned(int patternType, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color}
```
public void patterned(int patternType, Color foreColor, Color backColor)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| patternType | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Définit un objet Color qui représente la couleur d'arrière-plan du remplissage.

 **Examples:** 

Montre comment remplir une forme avec des dégradés.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | Un objet Color qui représente la couleur d'arrière-plan du remplissage. |

### setBackThemeColor(int value) {#setBackThemeColor-int}
```
public void setBackThemeColor(int value)
```


Définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage.

 **Examples:** 

Montre comment définir la couleur de thème pour la couleur de forme avant-plan/arrière-plan.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage. La valeur doit être l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackTintAndShade(double value) {#setBackTintAndShade-double}
```
public void setBackTintAndShade(double value)
```


Définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Définit un objet Color qui représente la couleur de premier plan du remplissage.

 **Remarks:** 

Cette propriété préserve le composant alpha du java.awt.Color, contrairement à la propriété [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color), qui le réinitialise à une couleur totalement opaque.

 **Examples:** 

Montre comment convertir n'importe quel remplissage en remplissage uni.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | Un objet Color qui représente la couleur de premier plan du remplissage. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Définit un objet Color qui représente la couleur de premier plan du remplissage.

 **Remarks:** 

Cette propriété réinitialise le composant alpha du java.awt.Color à une couleur totalement opaque, contrairement à la propriété [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color), qui le préserve.

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

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | Un objet Color qui représente la couleur de premier plan du remplissage. |

### setForeThemeColor(int value) {#setForeThemeColor-int}
```
public void setForeThemeColor(int value)
```


Définit un objet ThemeColor qui représente la couleur de premier plan du remplissage.

 **Examples:** 

Montre comment définir la couleur de thème pour la couleur de forme avant-plan/arrière-plan.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Un objet ThemeColor qui représente la couleur de premier plan du remplissage. La valeur doit être l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setForeTintAndShade(double value) {#setForeTintAndShade-double}
```
public void setForeTintAndShade(double value)
```


Définit une valeur double qui éclaircit ou assombrit la couleur de premier plan.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui éclaircit ou assombrit la couleur de premier plan. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```


Définit l'angle du remplissage en dégradé.

 **Examples:** 

Montre comment remplir une forme avec des dégradés.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | L'angle du remplissage en dégradé. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```


Modifie le type de remplissage en image unique.

 **Examples:** 

Montre comment définir le type de remplissage de forme comme image.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | Le tableau d'octets de l'image. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Modifie le type de remplissage en image unique.

 **Examples:** 

Montre comment définir le type de remplissage de forme comme image.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Le chemin du fichier image. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


Définit le degré d'opacité du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (transparent) et 1.0 (opaque).

 **Remarks:** 

Cette propriété est l'opposée de la propriété [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Montre comment remplir une forme avec une couleur unie.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Le degré d'opacité du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (transparent) et 1.0 (opaque). |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```


Définit si le remplissage tourne avec l'objet spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique si le remplissage tourne avec l'objet spécifié. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```


Définit l'alignement pour le remplissage de texture en mosaïque.

 **Examples:** 

Montre comment remplir et carreliser la texture à l'intérieur de la forme.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | L'alignement du remplissage de texture en mosaïque. La valeur doit être l'une des constantes [TextureAlignment](../../com.aspose.words/texturealignment/). |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Définit le degré de transparence du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (opaque) et 1.0 (transparent).

 **Remarks:** 

Cette propriété est l'opposée de la propriété [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Montre comment convertir n'importe quel remplissage en remplissage uni.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Le degré de transparence du remplissage spécifié sous forme d'une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


Définit la valeur qui est  true  si le formatage appliqué à cette instance est visible.

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

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Valeur qui est  true  si le formatage appliqué à cette instance est visible. |

### solid() {#solid}
```
public void solid()
```


Définit le remplissage à une couleur uniforme.

 **Remarks:** 

Utilisez cette méthode pour convertir n'importe quel remplissage en remplissage plein.

 **Examples:** 

Montre comment convertir n'importe quel remplissage en remplissage uni.

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


Définit le remplissage à une couleur uniforme spécifiée.

 **Remarks:** 

Utilisez cette méthode pour convertir n'importe quel remplissage en remplissage plein.

 **Examples:** 

Montre comment utiliser le formatage du graphique.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| couleur | java.awt.Color |  |

### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| style | int |  |
| variant | int |  |

