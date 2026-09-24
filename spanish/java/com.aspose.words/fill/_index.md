---
title: "Relleno"
linktitle: "Relleno"
second_title: "Aspose.Words para Java"
description: "Representa el formato de relleno para un objeto en Java."
type: docs
weight: 311
url: /es/java/com.aspose.words/fill/
---

**Inheritance:**
java.lang.Object
```
public class Fill
```

Representa el formato de relleno para un objeto.

Para obtener más información, visite el artículo de documentación [ Working with Graphic Elements ][Working with Graphic Elements].

 **Remarks:** 

Utiliza la propiedad [ShapeBase.getFill()](../../com.aspose.words/shapebase/\#getFill) o [Font.getFill()](../../com.aspose.words/font/\#getFill) para acceder a las propiedades de relleno de un objeto. No creas instancias de la clase [Fill](../../com.aspose.words/fill/) directamente.

 **Examples:** 

Muestra cómo rellenar una forma con un color sólido.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getBackColor()](#getBackColor) | Obtiene un objeto Color que representa el color de fondo del relleno. |
| [getBackThemeColor()](#getBackThemeColor) | Obtiene un objeto ThemeColor que representa el color de fondo del relleno. |
| [getBackTintAndShade()](#getBackTintAndShade) | Obtiene un valor double que aclara o oscurece el color de fondo. |
| [getBaseForeColor()](#getBaseForeColor) | Obtiene un objeto Color que representa el color de primer plano base del relleno sin ningún modificador. |
| [getColor()](#getColor) | Obtiene un objeto Color que representa el color de primer plano del relleno. |
| [getFillType()](#getFillType) | Obtiene un tipo de relleno. |
| [getForeColor()](#getForeColor) | Obtiene un objeto Color que representa el color de primer plano del relleno. |
| [getForeThemeColor()](#getForeThemeColor) | Obtiene un objeto ThemeColor que representa el color de primer plano del relleno. |
| [getForeTintAndShade()](#getForeTintAndShade) | Obtiene un valor double que aclara o oscurece el color de primer plano. |
| [getGradientAngle()](#getGradientAngle) | Obtiene el ángulo del relleno degradado. |
| [getGradientStops()](#getGradientStops) | Obtiene una colección de objetos [GradientStop](../../com.aspose.words/gradientstop/) para el relleno. |
| [getGradientStyle()](#getGradientStyle) | Obtiene el estilo de degradado [GradientStyle](../../com.aspose.words/gradientstyle/) para el relleno. |
| [getGradientVariant()](#getGradientVariant) | Obtiene la variante de degradado [GradientVariant](../../com.aspose.words/gradientvariant/) para el relleno. |
| [getImageBytes()](#getImageBytes) | Obtiene los bytes sin procesar de la textura o patrón de relleno. |
| [getOpacity()](#getOpacity) | Obtiene el grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco). |
| [getPattern()](#getPattern) | Obtiene un [PatternType](../../com.aspose.words/patterntype/) para el relleno. |
| [getPresetTexture()](#getPresetTexture) | Obtiene una [PresetTexture](../../com.aspose.words/presettexture/) para el relleno. |
| [getRotateWithObject()](#getRotateWithObject) | Obtiene si el relleno rota con el objeto especificado. |
| [getTextureAlignment()](#getTextureAlignment) | Obtiene la alineación para el relleno de textura de mosaico. |
| [getTransparency()](#getTransparency) | Obtiene el grado de transparencia del relleno especificado como un valor entre 0.0 (opaco) y 1.0 (transparente). |
| [getVisible()](#getVisible) | Obtiene el valor que es  true  si el formato aplicado a esta instancia es visible. |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [patterned(int patternType, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Establece un objeto Color que representa el color de fondo para el relleno. |
| [setBackThemeColor(int value)](#setBackThemeColor-int) | Establece un objeto ThemeColor que representa el color de fondo para el relleno. |
| [setBackTintAndShade(double value)](#setBackTintAndShade-double) | Establece un valor doble que aclara o oscurece el color de fondo. |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece un objeto Color que representa el color de primer plano para el relleno. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Establece un objeto Color que representa el color de primer plano para el relleno. |
| [setForeThemeColor(int value)](#setForeThemeColor-int) | Establece un objeto ThemeColor que representa el color de primer plano para el relleno. |
| [setForeTintAndShade(double value)](#setForeTintAndShade-double) | Establece un valor doble que aclara o oscurece el color de primer plano. |
| [setGradientAngle(double value)](#setGradientAngle-double) | Establece el ángulo del relleno degradado. |
| [setImage(byte[] imageBytes)](#setImage-byte) | Cambia el tipo de relleno a una sola imagen. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Cambia el tipo de relleno a una sola imagen. |
| [setOpacity(double value)](#setOpacity-double) | Establece el grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco). |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) | Establece si el relleno rota con el objeto especificado. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) | Establece la alineación para el relleno de textura de mosaico. |
| [setTransparency(double value)](#setTransparency-double) | Establece el grado de transparencia del relleno especificado como un valor entre 0.0 (opaco) y 1.0 (transparente). |
| [setVisible(boolean value)](#setVisible-boolean) | Establece el valor que es  true  si el formato aplicado a esta instancia es visible. |
| [solid()](#solid) | Establece el relleno a un color uniforme. |
| [solid(Color color)](#solid-java.awt.Color) | Establece el relleno a un color uniforme especificado. |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int) |  |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Obtiene un objeto Color que representa el color de fondo del relleno.

 **Examples:** 

Muestra cómo rellenar una forma con un degradado.

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
java.awt.Color - Un objeto Color que representa el color de fondo para el relleno.
### getBackThemeColor() {#getBackThemeColor}
```
public int getBackThemeColor()
```


Obtiene un objeto ThemeColor que representa el color de fondo del relleno.

 **Examples:** 

Muestra cómo establecer el color temático para el color de primer plano/fondo de la forma.

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
int - Un objeto ThemeColor que representa el color de fondo para el relleno. El valor devuelto es una de las constantes de [ThemeColor](../../com.aspose.words/themecolor/) .
### getBackTintAndShade() {#getBackTintAndShade}
```
public double getBackTintAndShade()
```


Obtiene un valor double que aclara o oscurece el color de fondo.

**Returns:**
double - Un valor double que aclara o oscurece el color de fondo.
### getBaseForeColor() {#getBaseForeColor}
```
public Color getBaseForeColor()
```


Obtiene un objeto Color que representa el color de primer plano base del relleno sin ningún modificador.

 **Examples:** 

Muestra cómo obtener el color de primer plano sin modificadores.

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
java.awt.Color - Un objeto Color que representa el color base de primer plano para el relleno sin ningún modificador.
### getColor() {#getColor}
```
public Color getColor()
```


Obtiene un objeto Color que representa el color de primer plano del relleno.

 **Remarks:** 

Esta propiedad conserva el componente alfa de java.awt.Color, a diferencia de la propiedad [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color), que lo restablece a un color totalmente opaco.

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

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
java.awt.Color - Un objeto Color que representa el color de primer plano para el relleno.
### getFillType() {#getFillType}
```
public int getFillType()
```


Obtiene un tipo de relleno.

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

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
int - Un tipo de relleno. El valor devuelto es una de las constantes de [FillType](../../com.aspose.words/filltype/) .
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Obtiene un objeto Color que representa el color de primer plano del relleno.

 **Remarks:** 

Esta propiedad restablece el componente alfa de java.awt.Color a un color totalmente opaco, a diferencia de la propiedad [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color), que lo conserva.

 **Examples:** 

Muestra para crear una variedad de formas.

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
java.awt.Color - Un objeto Color que representa el color de primer plano para el relleno.
### getForeThemeColor() {#getForeThemeColor}
```
public int getForeThemeColor()
```


Obtiene un objeto ThemeColor que representa el color de primer plano del relleno.

 **Examples:** 

Muestra cómo establecer el color temático para el color de primer plano/fondo de la forma.

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
int - Un objeto ThemeColor que representa el color de primer plano para el relleno. El valor devuelto es una de las constantes de [ThemeColor](../../com.aspose.words/themecolor/) .
### getForeTintAndShade() {#getForeTintAndShade}
```
public double getForeTintAndShade()
```


Obtiene un valor double que aclara o oscurece el color de primer plano.

**Returns:**
double - Un valor double que aclara o oscurece el color de primer plano.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```


Obtiene el ángulo del relleno degradado.

 **Examples:** 

Muestra cómo rellenar una forma con un degradado.

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
double - El ángulo del relleno degradado.
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```


Obtiene una colección de objetos [GradientStop](../../com.aspose.words/gradientstop/) para el relleno.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

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


Obtiene el estilo de degradado [GradientStyle](../../com.aspose.words/gradientstyle/) para el relleno.

 **Examples:** 

Muestra cómo rellenar una forma con un degradado.

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
int - El estilo de degradado [GradientStyle](../../com.aspose.words/gradientstyle/) para el relleno. El valor devuelto es una de las constantes de [GradientStyle](../../com.aspose.words/gradientstyle/) .
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```


Obtiene la variante de degradado [GradientVariant](../../com.aspose.words/gradientvariant/) para el relleno.

 **Examples:** 

Muestra cómo rellenar una forma con un degradado.

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
int - La variante de degradado [GradientVariant](../../com.aspose.words/gradientvariant/) para el relleno. El valor devuelto es una de las constantes de [GradientVariant](../../com.aspose.words/gradientvariant/) .
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Obtiene los bytes sin procesar de la textura o patrón de relleno.

 **Remarks:** 

El valor predeterminado es  null .

 **Examples:** 

Muestra para crear una variedad de formas.

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
byte[] - Los bytes sin procesar de la textura o patrón del relleno.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


Obtiene el grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco).

 **Remarks:** 

Esta propiedad es lo opuesto a la propiedad [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Muestra cómo rellenar una forma con un color sólido.

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
double - El grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco).
### getPattern() {#getPattern}
```
public int getPattern()
```


Obtiene un [PatternType](../../com.aspose.words/patterntype/) para el relleno.

 **Examples:** 

Muestra cómo establecer un patrón para una forma.

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
int - Un [PatternType](../../com.aspose.words/patterntype/) para el relleno. El valor devuelto es una de las constantes de [PatternType](../../com.aspose.words/patterntype/) .
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```


Obtiene una [PresetTexture](../../com.aspose.words/presettexture/) para el relleno.

 **Examples:** 

Muestra cómo rellenar y mosaicar la textura dentro de la forma.

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
int - Un [PresetTexture](../../com.aspose.words/presettexture/) para el relleno. El valor devuelto es una de las constantes de [PresetTexture](../../com.aspose.words/presettexture/) .
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```


Obtiene si el relleno rota con el objeto especificado.

**Returns:**
boolean - Si el relleno gira con el objeto especificado.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```


Obtiene la alineación para el relleno de textura de mosaico.

 **Examples:** 

Muestra cómo rellenar y mosaicar la textura dentro de la forma.

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
int - La alineación para el relleno de textura en mosaico. El valor devuelto es una de las constantes de [TextureAlignment](../../com.aspose.words/texturealignment/) .
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Obtiene el grado de transparencia del relleno especificado como un valor entre 0.0 (opaco) y 1.0 (transparente).

 **Remarks:** 

Esta propiedad es lo opuesto a la propiedad [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

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
double - El grado de transparencia del relleno especificado como un valor entre 0.0 (opaco) y 1.0 (claro).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Obtiene el valor que es  true  si el formato aplicado a esta instancia es visible.

 **Examples:** 

Muestra para crear una variedad de formas.

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
boolean - Valor que es  true  si el formato aplicado a esta instancia es visible.
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| estilo | int |  |
| variant | int |  |
| degree | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| color | java.awt.Color |  |
| estilo | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patternType | int |  |

### patterned(int patternType, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color}
```
public void patterned(int patternType, Color foreColor, Color backColor)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patternType | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| presetTexture | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Establece un objeto Color que representa el color de fondo para el relleno.

 **Examples:** 

Muestra cómo rellenar una forma con un degradado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | Un objeto Color que representa el color de fondo del relleno. |

### setBackThemeColor(int value) {#setBackThemeColor-int}
```
public void setBackThemeColor(int value)
```


Establece un objeto ThemeColor que representa el color de fondo para el relleno.

 **Examples:** 

Muestra cómo establecer el color temático para el color de primer plano/fondo de la forma.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un objeto ThemeColor que representa el color de fondo del relleno. El valor debe ser uno de los constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackTintAndShade(double value) {#setBackTintAndShade-double}
```
public void setBackTintAndShade(double value)
```


Establece un valor doble que aclara o oscurece el color de fondo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que aclara o oscurece el color de fondo. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Establece un objeto Color que representa el color de primer plano para el relleno.

 **Remarks:** 

Esta propiedad conserva el componente alfa de java.awt.Color, a diferencia de la propiedad [getForeColor()](../../com.aspose.words/fill/\#getForeColor) / [setForeColor(java.awt.Color)](../../com.aspose.words/fill/\#setForeColor-java.awt.Color), que lo restablece a un color totalmente opaco.

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | Un objeto Color que representa el color de primer plano del relleno. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Establece un objeto Color que representa el color de primer plano para el relleno.

 **Remarks:** 

Esta propiedad restablece el componente alfa de java.awt.Color a un color totalmente opaco, a diferencia de la propiedad [getColor()](../../com.aspose.words/fill/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color), que lo conserva.

 **Examples:** 

Muestra para crear una variedad de formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | Un objeto Color que representa el color de primer plano del relleno. |

### setForeThemeColor(int value) {#setForeThemeColor-int}
```
public void setForeThemeColor(int value)
```


Establece un objeto ThemeColor que representa el color de primer plano para el relleno.

 **Examples:** 

Muestra cómo establecer el color temático para el color de primer plano/fondo de la forma.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un objeto ThemeColor que representa el color de primer plano del relleno. El valor debe ser uno de los constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setForeTintAndShade(double value) {#setForeTintAndShade-double}
```
public void setForeTintAndShade(double value)
```


Establece un valor doble que aclara o oscurece el color de primer plano.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que aclara o oscurece el color de primer plano. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```


Establece el ángulo del relleno degradado.

 **Examples:** 

Muestra cómo rellenar una forma con un degradado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El ángulo del relleno degradado. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```


Cambia el tipo de relleno a una sola imagen.

 **Examples:** 

Muestra cómo establecer el tipo de relleno de forma como imagen.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | byte[] | La matriz de bytes de la imagen. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Cambia el tipo de relleno a una sola imagen.

 **Examples:** 

Muestra cómo establecer el tipo de relleno de forma como imagen.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | La ruta al archivo de imagen. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


Establece el grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco).

 **Remarks:** 

Esta propiedad es lo opuesto a la propiedad [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

 **Examples:** 

Muestra cómo rellenar una forma con un color sólido.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El grado de opacidad del relleno especificado como un valor entre 0.0 (claro) y 1.0 (opaco). |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```


Establece si el relleno rota con el objeto especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si el relleno rota con el objeto especificado. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```


Establece la alineación para el relleno de textura de mosaico.

 **Examples:** 

Muestra cómo rellenar y mosaicar la textura dentro de la forma.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La alineación para el relleno de textura en mosaico. El valor debe ser uno de los constantes [TextureAlignment](../../com.aspose.words/texturealignment/). |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Establece el grado de transparencia del relleno especificado como un valor entre 0.0 (opaco) y 1.0 (transparente).

 **Remarks:** 

Esta propiedad es lo opuesto a la propiedad [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El grado de transparencia del relleno especificado como un valor entre 0.0 (opaco) y 1.0 (claro). |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


Establece el valor que es  true  si el formato aplicado a esta instancia es visible.

 **Examples:** 

Muestra para crear una variedad de formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Valor que es  true  si el formato aplicado a esta instancia es visible. |

### solid() {#solid}
```
public void solid()
```


Establece el relleno a un color uniforme.

 **Remarks:** 

Utilice este método para convertir cualquiera de los rellenos de nuevo a relleno sólido.

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

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


Establece el relleno a un color uniforme especificado.

 **Remarks:** 

Utilice este método para convertir cualquiera de los rellenos de nuevo a relleno sólido.

 **Examples:** 

Muestra cómo usar el formato de gráfico.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| color | java.awt.Color |  |

### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| estilo | int |  |
| variant | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| estilo | int |  |
| variant | int |  |

