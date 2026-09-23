---
title: "Trait"
linktitle: "Trait"
second_title: "Aspose.Words pour Java"
description: "Définit un trait pour une forme en Java."
type: docs
weight: 636
url: /fr/java/com.aspose.words/stroke/
---

**Inheritance:**
java.lang.Object
```
public class Stroke
```

Définit un trait pour une forme.

Pour en savoir plus, consultez l'article de documentation [ Working with Shapes ][Working with Shapes].

 **Remarks:** 

Utilisez la propriété [Shape.getStroke()](../../com.aspose.words/shape/\#getStroke) pour accéder aux propriétés du trait d'une forme. Vous ne créez pas d'instances de la classe [Stroke](../../com.aspose.words/stroke/) directement.

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBackColor()](#getBackColor) | Obtient la couleur d'arrière-plan du trait. |
| [getBackThemeColor()](#getBackThemeColor) | Obtient un objet ThemeColor qui représente la couleur d'arrière-plan du trait. |
| [getBackTintAndShade()](#getBackTintAndShade) | Obtient une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait. |
| [getBaseForeColor()](#getBaseForeColor) | Obtient la couleur de premier plan de base du trait sans aucun modificateur. |
| [getColor()](#getColor) | Définit la couleur d'un trait. |
| [getColor2()](#getColor2) | Définit une seconde couleur pour un trait. |
| [getDashStyle()](#getDashStyle) | Spécifie le motif de points et de tirets d'un trait. |
| [getEndArrowLength()](#getEndArrowLength) | Définit la longueur de la pointe de flèche pour l'extrémité d'un trait. |
| [getEndArrowType()](#getEndArrowType) | Définit la pointe de flèche pour l'extrémité d'un trait. |
| [getEndArrowWidth()](#getEndArrowWidth) | Définit la largeur de la pointe de flèche pour l'extrémité d'un trait. |
| [getEndCap()](#getEndCap) | Définit le style de coiffe pour l'extrémité d'un trait. |
| [getFill()](#getFill) | Obtient le format de remplissage pour le [Stroke](../../com.aspose.words/stroke/). |
| [getFillType()](#getFillType) |  |
| [getFillableBackColor()](#getFillableBackColor) |  |
| [getFillableBackThemeColor()](#getFillableBackThemeColor) |  |
| [getFillableBackTintAndShade()](#getFillableBackTintAndShade) |  |
| [getFillableBaseForeColor()](#getFillableBaseForeColor) |  |
| [getFillableForeColor()](#getFillableForeColor) |  |
| [getFillableForeThemeColor()](#getFillableForeThemeColor) |  |
| [getFillableForeTintAndShade()](#getFillableForeTintAndShade) |  |
| [getFillableImageBytes()](#getFillableImageBytes) |  |
| [getFillableTransparency()](#getFillableTransparency) |  |
| [getFillableVisible()](#getFillableVisible) |  |
| [getFilledColor()](#getFilledColor) |  |
| [getForeColor()](#getForeColor) | Obtient la couleur de premier plan du trait. |
| [getForeThemeColor()](#getForeThemeColor) | Obtient un objet ThemeColor qui représente la couleur de premier plan du trait. |
| [getForeTintAndShade()](#getForeTintAndShade) | Obtient une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait. |
| [getGradientAngle()](#getGradientAngle) |  |
| [getGradientStops()](#getGradientStops) |  |
| [getGradientStyle()](#getGradientStyle) |  |
| [getGradientVariant()](#getGradientVariant) |  |
| [getImageBytes()](#getImageBytes) | Définit l'image pour un remplissage d'image ou de motif de trait. |
| [getJoinStyle()](#getJoinStyle) | Définit le style de jointure d'une polyligne. |
| [getLineStyle()](#getLineStyle) | Définit le style de ligne du trait. |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getOn()](#getOn) | Définit si le chemin sera tracé. |
| [getOpacity()](#getOpacity) | Définit le degré de transparence d'un trait. |
| [getPatternType()](#getPatternType) |  |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getStartArrowLength()](#getStartArrowLength) | Définit la longueur de la pointe de flèche pour le début d'un trait. |
| [getStartArrowType()](#getStartArrowType) | Définit la pointe de flèche pour le début d'un trait. |
| [getStartArrowWidth()](#getStartArrowWidth) | Définit la largeur de la pointe de flèche pour le début d'un trait. |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getTransparency()](#getTransparency) | Obtient une valeur entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence du trait. |
| [getVisible()](#getVisible) | Obtient un indicateur indiquant si le trait est visible. |
| [getWeight()](#getWeight) | Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points. |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Définit la couleur d'arrière-plan du trait. |
| [setBackThemeColor(int value)](#setBackThemeColor-int) | Définit un objet ThemeColor qui représente la couleur d'arrière-plan du trait. |
| [setBackTintAndShade(double value)](#setBackTintAndShade-double) | Définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait. |
| [setColor(Color value)](#setColor-java.awt.Color) | Définit la couleur d'un trait. |
| [setColor2(Color value)](#setColor2-java.awt.Color) | Définit une seconde couleur pour un trait. |
| [setDashStyle(int value)](#setDashStyle-int) | Spécifie le motif de points et de tirets d'un trait. |
| [setEndArrowLength(int value)](#setEndArrowLength-int) | Définit la longueur de la pointe de flèche pour l'extrémité d'un trait. |
| [setEndArrowType(int value)](#setEndArrowType-int) | Définit la pointe de flèche pour l'extrémité d'un trait. |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int) | Définit la largeur de la pointe de flèche pour l'extrémité d'un trait. |
| [setEndCap(int value)](#setEndCap-int) | Définit le style de coiffe pour l'extrémité d'un trait. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color) |  |
| [setFillableBackThemeColor(int value)](#setFillableBackThemeColor-int) |  |
| [setFillableBackTintAndShade(double value)](#setFillableBackTintAndShade-double) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color) |  |
| [setFillableForeThemeColor(int value)](#setFillableForeThemeColor-int) |  |
| [setFillableForeTintAndShade(double value)](#setFillableForeTintAndShade-double) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color) |  |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Définit la couleur de premier plan du trait. |
| [setForeThemeColor(int value)](#setForeThemeColor-int) | Définit un objet ThemeColor qui représente la couleur de premier plan du trait. |
| [setForeTintAndShade(double value)](#setForeTintAndShade-double) | Définit une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait. |
| [setGradientAngle(double value)](#setGradientAngle-double) |  |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setJoinStyle(int value)](#setJoinStyle-int) | Définit le style de jointure d'une polyligne. |
| [setLineStyle(int value)](#setLineStyle-int) | Définit le style de ligne du trait. |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setOn(boolean value)](#setOn-boolean) | Définit si le chemin sera tracé. |
| [setOpacity(double value)](#setOpacity-double) | Définit le degré de transparence d'un trait. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setStartArrowLength(int value)](#setStartArrowLength-int) | Définit la longueur de la pointe de flèche pour le début d'un trait. |
| [setStartArrowType(int value)](#setStartArrowType-int) | Définit la pointe de flèche pour le début d'un trait. |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int) | Définit la largeur de la pointe de flèche pour le début d'un trait. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setTransparency(double value)](#setTransparency-double) | Définit une valeur entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence du trait. |
| [setVisible(boolean value)](#setVisible-boolean) | Définit un indicateur indiquant si le trait est visible. |
| [setWeight(double value)](#setWeight-double) | Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points. |
| [solid()](#solid) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Obtient la couleur d'arrière-plan du trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getWhite().getWhite().

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Returns:**
java.awt.Color - La couleur d'arrière-plan du trait.
### getBackThemeColor() {#getBackThemeColor}
```
public int getBackThemeColor()
```


Obtient un objet ThemeColor qui représente la couleur d'arrière-plan du trait.

 **Examples:** 

Montre comment rétablir la couleur du thème ainsi que la teinte et l'ombrage.

```

 Document doc = new Document(getMyDir() + "Stroke gradient outline.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Stroke stroke = shape.getStroke();
 stroke.setBackThemeColor(ThemeColor.DARK_2);
 stroke.setBackTintAndShade(0.2d);

 doc.save(getArtifactsDir() + "Shape.StrokeBackThemeColors.docx");
 
```

**Returns:**
int - Un objet ThemeColor qui représente la couleur d'arrière-plan du trait. La valeur renvoyée est l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getBackTintAndShade() {#getBackTintAndShade}
```
public double getBackTintAndShade()
```


Obtient une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait.

 **Remarks:** 

Les valeurs autorisées sont comprises dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété à une valeur inférieure à -1 ou supérieure à 1 entraîne java.lang.IllegalArgumentException.

 **Examples:** 

Montre comment rétablir la couleur du thème ainsi que la teinte et l'ombrage.

```

 Document doc = new Document(getMyDir() + "Stroke gradient outline.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Stroke stroke = shape.getStroke();
 stroke.setBackThemeColor(ThemeColor.DARK_2);
 stroke.setBackTintAndShade(0.2d);

 doc.save(getArtifactsDir() + "Shape.StrokeBackThemeColors.docx");
 
```

**Returns:**
double - Une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait.
### getBaseForeColor() {#getBaseForeColor}
```
public Color getBaseForeColor()
```


Obtient la couleur de premier plan de base du trait sans aucun modificateur.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getBlack().getBlack().

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
java.awt.Color - La couleur de premier plan de base du trait sans aucun modificateur.
### getColor() {#getColor}
```
public Color getColor()
```


Définit la couleur d'un trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getBlack().getBlack().

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
java.awt.Color - La valeur java.awt.Color correspondante.
### getColor2() {#getColor2}
```
public Color getColor2()
```


Définit une seconde couleur pour un trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getWhite().getWhite().

 **Examples:** 

Montre comment traiter les fonctionnalités de trait de forme.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 Stroke stroke = shape.getStroke();

 // Strokes can have two colors, which are used to create a pattern defined by two-tone image data.
 // Strokes with a single color do not use the Color2 property.
 Assert.assertEquals(new Color((128), (0), (0), (255)), stroke.getColor());
 Assert.assertEquals(new Color((255), (255), (0), (255)), stroke.getColor2());

 Assert.assertNotNull(stroke.getImageBytes());
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Drawing.StrokePattern.png"), stroke.getImageBytes());
 
```

**Returns:**
java.awt.Color - La valeur java.awt.Color correspondante.
### getDashStyle() {#getDashStyle}
```
public int getDashStyle()
```


Spécifie le motif de points et de tirets d'un trait.

 **Remarks:** 

La valeur par défaut est [DashStyle.SOLID](../../com.aspose.words/dashstyle/\#SOLID).

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
int - La valeur int correspondante. La valeur renvoyée est l'une des constantes [DashStyle](../../com.aspose.words/dashstyle/).
### getEndArrowLength() {#getEndArrowLength}
```
public int getEndArrowLength()
```


Définit la longueur de la pointe de flèche pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength/\#MEDIUM).

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
int - La valeur int correspondante. La valeur renvoyée est l'une des constantes [ArrowLength](../../com.aspose.words/arrowlength/).
### getEndArrowType() {#getEndArrowType}
```
public int getEndArrowType()
```


Définit la pointe de flèche pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowType.NONE](../../com.aspose.words/arrowtype/\#NONE).

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
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [ArrowType](../../com.aspose.words/arrowtype/).
### getEndArrowWidth() {#getEndArrowWidth}
```
public int getEndArrowWidth()
```


Définit la largeur de la pointe de flèche pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth/\#MEDIUM).

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
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [ArrowWidth](../../com.aspose.words/arrowwidth/).
### getEndCap() {#getEndCap}
```
public int getEndCap()
```


Définit le style de coiffe pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [EndCap.FLAT](../../com.aspose.words/endcap/\#FLAT).

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
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [EndCap](../../com.aspose.words/endcap/).
### getFill() {#getFill}
```
public Fill getFill()
```


Obtient le format de remplissage pour le [Stroke](../../com.aspose.words/stroke/).

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Returns:**
[Fill](../../com.aspose.words/fill/) - Fill formatting for the [Stroke](../../com.aspose.words/stroke/).
### getFillType() {#getFillType}
```
public int getFillType()
```




**Returns:**
int
### getFillableBackColor() {#getFillableBackColor}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### getFillableBackThemeColor() {#getFillableBackThemeColor}
```
public int getFillableBackThemeColor()
```




**Returns:**
int
### getFillableBackTintAndShade() {#getFillableBackTintAndShade}
```
public double getFillableBackTintAndShade()
```




**Returns:**
double
### getFillableBaseForeColor() {#getFillableBaseForeColor}
```
public Color getFillableBaseForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeColor() {#getFillableForeColor}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeThemeColor() {#getFillableForeThemeColor}
```
public int getFillableForeThemeColor()
```




**Returns:**
int
### getFillableForeTintAndShade() {#getFillableForeTintAndShade}
```
public double getFillableForeTintAndShade()
```




**Returns:**
double
### getFillableImageBytes() {#getFillableImageBytes}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableTransparency() {#getFillableTransparency}
```
public double getFillableTransparency()
```




**Returns:**
double
### getFillableVisible() {#getFillableVisible}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### getFilledColor() {#getFilledColor}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Obtient la couleur de premier plan du trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Returns:**
java.awt.Color - La couleur de premier plan du trait.
### getForeThemeColor() {#getForeThemeColor}
```
public int getForeThemeColor()
```


Obtient un objet ThemeColor qui représente la couleur de premier plan du trait.

 **Examples:** 

Montre comment définir la couleur de thème de premier plan ainsi que la teinte et l'ombrage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 40.0);
 Stroke stroke = shape.getStroke();
 stroke.setForeThemeColor(ThemeColor.DARK_1);
 stroke.setForeTintAndShade(0.5);

 doc.save(getArtifactsDir() + "Shape.StrokeForeThemeColors.docx");
 
```

**Returns:**
int - Un objet ThemeColor qui représente la couleur de premier plan du trait. La valeur renvoyée est l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getForeTintAndShade() {#getForeTintAndShade}
```
public double getForeTintAndShade()
```


Obtient une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait.

 **Remarks:** 

Les valeurs autorisées sont comprises dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété à une valeur inférieure à -1 ou supérieure à 1 entraîne java.lang.IllegalArgumentException.

 **Examples:** 

Montre comment définir la couleur de thème de premier plan ainsi que la teinte et l'ombrage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 40.0);
 Stroke stroke = shape.getStroke();
 stroke.setForeThemeColor(ThemeColor.DARK_1);
 stroke.setForeTintAndShade(0.5);

 doc.save(getArtifactsDir() + "Shape.StrokeForeThemeColors.docx");
 
```

**Returns:**
double - Une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```




**Returns:**
double
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/)
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```




**Returns:**
int
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Définit l'image pour un remplissage d'image ou de motif de trait.

 **Examples:** 

Montre comment traiter les fonctionnalités de trait de forme.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 Stroke stroke = shape.getStroke();

 // Strokes can have two colors, which are used to create a pattern defined by two-tone image data.
 // Strokes with a single color do not use the Color2 property.
 Assert.assertEquals(new Color((128), (0), (0), (255)), stroke.getColor());
 Assert.assertEquals(new Color((255), (255), (0), (255)), stroke.getColor2());

 Assert.assertNotNull(stroke.getImageBytes());
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Drawing.StrokePattern.png"), stroke.getImageBytes());
 
```

**Returns:**
byte[] - La valeur byte[] correspondante.
### getJoinStyle() {#getJoinStyle}
```
public int getJoinStyle()
```


Définit le style de jointure d'une polyligne.

 **Remarks:** 

La valeur par défaut est [JoinStyle.ROUND](../../com.aspose.words/joinstyle/\#ROUND).

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [JoinStyle](../../com.aspose.words/joinstyle/).
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Définit le style de ligne du trait.

 **Remarks:** 

La valeur par défaut est [ShapeLineStyle.SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [ShapeLineStyle](../../com.aspose.words/shapelinestyle/).
### getOldOn() {#getOldOn}
```
public boolean getOldOn()
```




**Returns:**
boolean
### getOldOpacity() {#getOldOpacity}
```
public double getOldOpacity()
```




**Returns:**
double
### getOn() {#getOn}
```
public boolean getOn()
```


Définit si le chemin sera tracé.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est  true .

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


Définit le degré de transparence d'un trait. La plage valide est de 0 à 1.

 **Remarks:** 

La valeur par défaut est 1.

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
double - La valeur  double  correspondante.
### getPatternType() {#getPatternType}
```
public int getPatternType()
```




**Returns:**
int
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```




**Returns:**
int
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### getStartArrowLength() {#getStartArrowLength}
```
public int getStartArrowLength()
```


Définit la longueur de la pointe de flèche pour le début d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength/\#MEDIUM).

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
int - La valeur int correspondante. La valeur renvoyée est l'une des constantes [ArrowLength](../../com.aspose.words/arrowlength/).
### getStartArrowType() {#getStartArrowType}
```
public int getStartArrowType()
```


Définit la pointe de flèche pour le début d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowType.NONE](../../com.aspose.words/arrowtype/\#NONE).

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
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [ArrowType](../../com.aspose.words/arrowtype/).
### getStartArrowWidth() {#getStartArrowWidth}
```
public int getStartArrowWidth()
```


Définit la largeur de la pointe de flèche pour le début d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth/\#MEDIUM).

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
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [ArrowWidth](../../com.aspose.words/arrowwidth/).
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```




**Returns:**
int
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Obtient une valeur entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence du trait.

 **Remarks:** 

La valeur par défaut est 0.

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Returns:**
double - Une valeur entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence du trait.
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Obtient un indicateur indiquant si le trait est visible.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est  true .

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Returns:**
boolean - Un indicateur indiquant si le trait est visible.
### getWeight() {#getWeight}
```
public double getWeight()
```


Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est 0.75.

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Returns:**
double - La valeur  double  correspondante.
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

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| patternType | int |  |

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


Définit la couleur d'arrière-plan du trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getWhite().getWhite().

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La couleur d'arrière-plan du trait. |

### setBackThemeColor(int value) {#setBackThemeColor-int}
```
public void setBackThemeColor(int value)
```


Définit un objet ThemeColor qui représente la couleur d'arrière-plan du trait.

 **Examples:** 

Montre comment rétablir la couleur du thème ainsi que la teinte et l'ombrage.

```

 Document doc = new Document(getMyDir() + "Stroke gradient outline.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Stroke stroke = shape.getStroke();
 stroke.setBackThemeColor(ThemeColor.DARK_2);
 stroke.setBackTintAndShade(0.2d);

 doc.save(getArtifactsDir() + "Shape.StrokeBackThemeColors.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Un objet ThemeColor qui représente la couleur d'arrière-plan du trait. La valeur doit être l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackTintAndShade(double value) {#setBackTintAndShade-double}
```
public void setBackTintAndShade(double value)
```


Définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait.

 **Remarks:** 

Les valeurs autorisées sont comprises dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété à une valeur inférieure à -1 ou supérieure à 1 entraîne java.lang.IllegalArgumentException.

 **Examples:** 

Montre comment rétablir la couleur du thème ainsi que la teinte et l'ombrage.

```

 Document doc = new Document(getMyDir() + "Stroke gradient outline.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Stroke stroke = shape.getStroke();
 stroke.setBackThemeColor(ThemeColor.DARK_2);
 stroke.setBackTintAndShade(0.2d);

 doc.save(getArtifactsDir() + "Shape.StrokeBackThemeColors.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Définit la couleur d'un trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getBlack().getBlack().

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
| valeur | java.awt.Color | La valeur java.awt.Color correspondante. |

### setColor2(Color value) {#setColor2-java.awt.Color}
```
public void setColor2(Color value)
```


Définit une seconde couleur pour un trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getWhite().getWhite().

 **Examples:** 

Montre comment traiter les fonctionnalités de trait de forme.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 Stroke stroke = shape.getStroke();

 // Strokes can have two colors, which are used to create a pattern defined by two-tone image data.
 // Strokes with a single color do not use the Color2 property.
 Assert.assertEquals(new Color((128), (0), (0), (255)), stroke.getColor());
 Assert.assertEquals(new Color((255), (255), (0), (255)), stroke.getColor2());

 Assert.assertNotNull(stroke.getImageBytes());
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Drawing.StrokePattern.png"), stroke.getImageBytes());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La valeur java.awt.Color correspondante. |

### setDashStyle(int value) {#setDashStyle-int}
```
public void setDashStyle(int value)
```


Spécifie le motif de points et de tirets d'un trait.

 **Remarks:** 

La valeur par défaut est [DashStyle.SOLID](../../com.aspose.words/dashstyle/\#SOLID).

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
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [DashStyle](../../com.aspose.words/dashstyle/). |

### setEndArrowLength(int value) {#setEndArrowLength-int}
```
public void setEndArrowLength(int value)
```


Définit la longueur de la pointe de flèche pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength/\#MEDIUM).

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
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [ArrowLength](../../com.aspose.words/arrowlength/). |

### setEndArrowType(int value) {#setEndArrowType-int}
```
public void setEndArrowType(int value)
```


Définit la pointe de flèche pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowType.NONE](../../com.aspose.words/arrowtype/\#NONE).

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
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [ArrowType](../../com.aspose.words/arrowtype/). |

### setEndArrowWidth(int value) {#setEndArrowWidth-int}
```
public void setEndArrowWidth(int value)
```


Définit la largeur de la pointe de flèche pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth/\#MEDIUM).

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
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [ArrowWidth](../../com.aspose.words/arrowwidth/). |

### setEndCap(int value) {#setEndCap-int}
```
public void setEndCap(int value)
```


Définit le style de coiffe pour l'extrémité d'un trait.

 **Remarks:** 

La valeur par défaut est [EndCap.FLAT](../../com.aspose.words/endcap/\#FLAT).

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
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [EndCap](../../com.aspose.words/endcap/). |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color |  |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Définit la couleur de premier plan du trait.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La couleur de premier plan du trait. |

### setForeThemeColor(int value) {#setForeThemeColor-int}
```
public void setForeThemeColor(int value)
```


Définit un objet ThemeColor qui représente la couleur de premier plan du trait.

 **Examples:** 

Montre comment définir la couleur de thème de premier plan ainsi que la teinte et l'ombrage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 40.0);
 Stroke stroke = shape.getStroke();
 stroke.setForeThemeColor(ThemeColor.DARK_1);
 stroke.setForeTintAndShade(0.5);

 doc.save(getArtifactsDir() + "Shape.StrokeForeThemeColors.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Un objet ThemeColor qui représente la couleur de premier plan du trait. La valeur doit être l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setForeTintAndShade(double value) {#setForeTintAndShade-double}
```
public void setForeTintAndShade(double value)
```


Définit une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait.

 **Remarks:** 

Les valeurs autorisées sont comprises dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété à une valeur inférieure à -1 ou supérieure à 1 entraîne java.lang.IllegalArgumentException.

 **Examples:** 

Montre comment définir la couleur de thème de premier plan ainsi que la teinte et l'ombrage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 40.0);
 Stroke stroke = shape.getStroke();
 stroke.setForeThemeColor(ThemeColor.DARK_1);
 stroke.setForeTintAndShade(0.5);

 doc.save(getArtifactsDir() + "Shape.StrokeForeThemeColors.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double |  |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setJoinStyle(int value) {#setJoinStyle-int}
```
public void setJoinStyle(int value)
```


Définit le style de jointure d'une polyligne.

 **Remarks:** 

La valeur par défaut est [JoinStyle.ROUND](../../com.aspose.words/joinstyle/\#ROUND).

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [JoinStyle](../../com.aspose.words/joinstyle/). |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Définit le style de ligne du trait.

 **Remarks:** 

La valeur par défaut est [ShapeLineStyle.SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [ShapeLineStyle](../../com.aspose.words/shapelinestyle/). |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double |  |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```


Définit si le chemin sera tracé.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est  true .

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


Définit le degré de transparence d'un trait. La plage valide est de 0 à 1.

 **Remarks:** 

La valeur par défaut est 1.

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
| valeur | double | La valeur  double  correspondante. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean |  |

### setStartArrowLength(int value) {#setStartArrowLength-int}
```
public void setStartArrowLength(int value)
```


Définit la longueur de la pointe de flèche pour le début d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength/\#MEDIUM).

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
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [ArrowLength](../../com.aspose.words/arrowlength/). |

### setStartArrowType(int value) {#setStartArrowType-int}
```
public void setStartArrowType(int value)
```


Définit la pointe de flèche pour le début d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowType.NONE](../../com.aspose.words/arrowtype/\#NONE).

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
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [ArrowType](../../com.aspose.words/arrowtype/). |

### setStartArrowWidth(int value) {#setStartArrowWidth-int}
```
public void setStartArrowWidth(int value)
```


Définit la largeur de la pointe de flèche pour le début d'un trait.

 **Remarks:** 

La valeur par défaut est [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth/\#MEDIUM).

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
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [ArrowWidth](../../com.aspose.words/arrowwidth/). |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int |  |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Définit une valeur entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence du trait.

 **Remarks:** 

La valeur par défaut est 0.

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence du trait. |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


Définit un indicateur indiquant si le trait est visible.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est  true .

 **Examples:** 

Montre comment définir le format du marqueur.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Un indicateur indiquant si le trait est visible. |

### setWeight(double value) {#setWeight-double}
```
public void setWeight(double value)
```


Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points.

 **Remarks:** 

La valeur par défaut pour un [Shape](../../com.aspose.words/shape/) est 0.75.

 **Examples:** 

Montre comment modifier les propriétés du trait.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La valeur  double  correspondante. |

### solid() {#solid}
```
public void solid()
```




### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

