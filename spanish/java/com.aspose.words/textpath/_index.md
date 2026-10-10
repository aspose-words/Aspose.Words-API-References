---
title: "TextPath"
linktitle: "TextPath"
second_title: "Aspose.Words para Java"
description: "Define el texto y el formato de la ruta de texto de un objeto WordArt en Java."
type: docs
weight: 676
url: /es/java/com.aspose.words/textpath/
---

**Inheritance:**
java.lang.Object
```
public class TextPath
```

Define el texto y el formato de la ruta de texto (de un objeto WordArt).

Para obtener más información, visite el artículo de documentación [ Working with Shapes ][Working with Shapes].

 **Remarks:** 

Utilice la propiedad [Shape.getTextPath()](../../com.aspose.words/shape/\#getTextPath) para acceder a las propiedades WordArt de un shape. No crea instancias de la clase [TextPath](../../com.aspose.words/textpath/) directamente.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Métodos

| Método | Descripción |
| --- | --- |
| [getBold()](#getBold) | True si la fuente está formateada en negrita. |
| [getFitPath()](#getFitPath) | Define si el texto se ajusta a la ruta de un shape. |
| [getFitShape()](#getFitShape) | Define si el texto cabe en el cuadro delimitador de una forma. |
| [getFontFamily()](#getFontFamily) | Define la familia de la fuente del trazado de texto. |
| [getItalic()](#getItalic) | Verdadero si la fuente está formateada en cursiva. |
| [getKerning()](#getKerning) | Determina si el interletraje está activado. |
| [getOn()](#getOn) | Define si el texto se muestra. |
| [getReverseRows()](#getReverseRows) | Determina si el orden de disposición de las filas está invertido. |
| [getRotateLetters()](#getRotateLetters) | Determina si las letras del texto están rotadas. |
| [getSameLetterHeights()](#getSameLetterHeights) | Determina si todas las letras tendrán la misma altura sin importar el caso inicial. |
| [getShadow()](#getShadow) | Define si se aplica una sombra al texto en un trazado de texto. |
| [getSize()](#getSize) | Define el tamaño de la fuente en puntos. |
| [getSmallCaps()](#getSmallCaps) | Verdadero si la fuente está formateada en letras capitales pequeñas. |
| [getSpacing()](#getSpacing) | Define la cantidad de espaciado para el texto. |
| [getStrikeThrough()](#getStrikeThrough) | Verdadero si la fuente está formateada como texto tachado. |
| [getText()](#getText) | Define el texto del trazado de texto. |
| [getTextPathAlignment()](#getTextPathAlignment) | Define la alineación del texto. |
| [getTrim()](#getTrim) | Determina si se elimina el espacio extra arriba y abajo del texto. |
| [getUnderline()](#getUnderline) | Verdadero si la fuente está subrayada. |
| [getXScale()](#getXScale) | Determina si se usará un trazado de texto recto en lugar del trazado de forma. |
| [setBold(boolean value)](#setBold-boolean) | True si la fuente está formateada en negrita. |
| [setFitPath(boolean value)](#setFitPath-boolean) | Define si el texto se ajusta a la ruta de un shape. |
| [setFitShape(boolean value)](#setFitShape-boolean) | Define si el texto cabe en el cuadro delimitador de una forma. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Define la familia de la fuente del trazado de texto. |
| [setItalic(boolean value)](#setItalic-boolean) | Verdadero si la fuente está formateada en cursiva. |
| [setKerning(boolean value)](#setKerning-boolean) | Determina si el interletraje está activado. |
| [setOn(boolean value)](#setOn-boolean) | Define si el texto se muestra. |
| [setReverseRows(boolean value)](#setReverseRows-boolean) | Determina si el orden de disposición de las filas está invertido. |
| [setRotateLetters(boolean value)](#setRotateLetters-boolean) | Determina si las letras del texto están rotadas. |
| [setSameLetterHeights(boolean value)](#setSameLetterHeights-boolean) | Determina si todas las letras tendrán la misma altura sin importar el caso inicial. |
| [setShadow(boolean value)](#setShadow-boolean) | Define si se aplica una sombra al texto en un trazado de texto. |
| [setSize(double value)](#setSize-double) | Define el tamaño de la fuente en puntos. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | Verdadero si la fuente está formateada en letras capitales pequeñas. |
| [setSpacing(double value)](#setSpacing-double) | Define la cantidad de espaciado para el texto. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | Verdadero si la fuente está formateada como texto tachado. |
| [setText(String value)](#setText-java.lang.String) | Define el texto del trazado de texto. |
| [setTextPathAlignment(int value)](#setTextPathAlignment-int) | Define la alineación del texto. |
| [setTrim(boolean value)](#setTrim-boolean) | Determina si se elimina el espacio extra arriba y abajo del texto. |
| [setUnderline(boolean value)](#setUnderline-boolean) | Verdadero si la fuente está subrayada. |
| [setXScale(boolean value)](#setXScale-boolean) | Determina si se usará un trazado de texto recto en lugar del trazado de forma. |
### getBold() {#getBold}
```
public boolean getBold()
```


True si la fuente está formateada en negrita.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getFitPath() {#getFitPath}
```
public boolean getFitPath()
```


Define si el texto se ajusta a la ruta de un shape.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getFitShape() {#getFitShape}
```
public boolean getFitShape()
```


Define si el texto cabe en el cuadro delimitador de una forma.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Define la familia de la fuente del trazado de texto.

 **Remarks:** 

El valor predeterminado es Arial.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Verdadero si la fuente está formateada en cursiva.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getKerning() {#getKerning}
```
public boolean getKerning()
```


Determina si el interletraje está activado.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getOn() {#getOn}
```
public boolean getOn()
```


Define si el texto se muestra.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getReverseRows() {#getReverseRows}
```
public boolean getReverseRows()
```


Determina si el orden de disposición de las filas está invertido.

 **Remarks:** 

El valor predeterminado es  false .

Si verdadero, el orden de disposición de las filas está invertido. Este atributo se usa para la disposición de texto vertical.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getRotateLetters() {#getRotateLetters}
```
public boolean getRotateLetters()
```


Determina si las letras del texto están rotadas.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSameLetterHeights() {#getSameLetterHeights}
```
public boolean getSameLetterHeights()
```


Determina si todas las letras tendrán la misma altura sin importar el caso inicial.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Define si se aplica una sombra al texto en un trazado de texto.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSize() {#getSize}
```
public double getSize()
```


Define el tamaño de la fuente en puntos.

 **Remarks:** 

El valor predeterminado es 36.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
double - El valor  double  correspondiente.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


Verdadero si la fuente está formateada en letras capitales pequeñas.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Define la cantidad de espaciado para el texto. 1 significa 100%.

 **Remarks:** 

El valor predeterminado es 1.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
double - El valor  double  correspondiente.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


Verdadero si la fuente está formateada como texto tachado.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getText() {#getText}
```
public String getText()
```


Define el texto del trazado de texto.

 **Remarks:** 

El valor predeterminado es una cadena vacía.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getTextPathAlignment() {#getTextPathAlignment}
```
public int getTextPathAlignment()
```


Define la alineación del texto.

 **Remarks:** 

El valor predeterminado es [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER).

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [TextPathAlignment](../../com.aspose.words/textpathalignment/).
### getTrim() {#getTrim}
```
public boolean getTrim()
```


Determina si se elimina el espacio extra arriba y abajo del texto.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getUnderline() {#getUnderline}
```
public boolean getUnderline()
```


Verdadero si la fuente está subrayada.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getXScale() {#getXScale}
```
public boolean getXScale()
```


Determina si se usará un trazado de texto recto en lugar del trazado de forma.

 **Remarks:** 

El valor predeterminado es  false .

Si  true , el texto se desplaza a lo largo de una ruta de izquierda a derecha siguiendo el valor x del límite inferior de la forma.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True si la fuente está formateada en negrita.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setFitPath(boolean value) {#setFitPath-boolean}
```
public void setFitPath(boolean value)
```


Define si el texto se ajusta a la ruta de un shape.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setFitShape(boolean value) {#setFitShape-boolean}
```
public void setFitShape(boolean value)
```


Define si el texto cabe en el cuadro delimitador de una forma.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Define la familia de la fuente del trazado de texto.

 **Remarks:** 

El valor predeterminado es Arial.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Verdadero si la fuente está formateada en cursiva.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setKerning(boolean value) {#setKerning-boolean}
```
public void setKerning(boolean value)
```


Determina si el interletraje está activado.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```


Define si el texto se muestra.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setReverseRows(boolean value) {#setReverseRows-boolean}
```
public void setReverseRows(boolean value)
```


Determina si el orden de disposición de las filas está invertido.

 **Remarks:** 

El valor predeterminado es  false .

Si verdadero, el orden de disposición de las filas está invertido. Este atributo se usa para la disposición de texto vertical.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setRotateLetters(boolean value) {#setRotateLetters-boolean}
```
public void setRotateLetters(boolean value)
```


Determina si las letras del texto están rotadas.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSameLetterHeights(boolean value) {#setSameLetterHeights-boolean}
```
public void setSameLetterHeights(boolean value)
```


Determina si todas las letras tendrán la misma altura sin importar el caso inicial.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Define si se aplica una sombra al texto en un trazado de texto.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Define el tamaño de la fuente en puntos.

 **Remarks:** 

El valor predeterminado es 36.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor  double  correspondiente. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


Verdadero si la fuente está formateada en letras capitales pequeñas.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Define la cantidad de espaciado para el texto. 1 significa 100%.

 **Remarks:** 

El valor predeterminado es 1.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor  double  correspondiente. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


Verdadero si la fuente está formateada como texto tachado.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Define el texto del trazado de texto.

 **Remarks:** 

El valor predeterminado es una cadena vacía.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setTextPathAlignment(int value) {#setTextPathAlignment-int}
```
public void setTextPathAlignment(int value)
```


Define la alineación del texto.

 **Remarks:** 

El valor predeterminado es [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER).

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes de [TextPathAlignment](../../com.aspose.words/textpathalignment/). |

### setTrim(boolean value) {#setTrim-boolean}
```
public void setTrim(boolean value)
```


Determina si se elimina el espacio extra arriba y abajo del texto.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setUnderline(boolean value) {#setUnderline-boolean}
```
public void setUnderline(boolean value)
```


Verdadero si la fuente está subrayada.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setXScale(boolean value) {#setXScale-boolean}
```
public void setXScale(boolean value)
```


Determina si se usará un trazado de texto recto en lugar del trazado de forma.

 **Remarks:** 

El valor predeterminado es  false .

Si  true , el texto se desplaza a lo largo de una ruta de izquierda a derecha siguiendo el valor x del límite inferior de la forma.

 **Examples:** 

Muestra cómo trabajar con WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

