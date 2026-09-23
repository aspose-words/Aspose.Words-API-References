---
title: "TextPath"
linktitle: "TextPath"
second_title: "Aspose.Words per Java"
description: "Definisce il testo e la formattazione del percorso di testo di un oggetto WordArt in Java."
type: docs
weight: 676
url: /it/java/com.aspose.words/textpath/
---

**Inheritance:**
java.lang.Object
```
public class TextPath
```

Definisce il testo e la formattazione del percorso di testo (di un oggetto WordArt).

Per saperne di più, visita l'articolo di documentazione [ Working with Shapes ][Working with Shapes].

 **Remarks:** 

Usa la proprietà [Shape.getTextPath()](../../com.aspose.words/shape/\#getTextPath) per accedere alle proprietà WordArt di una forma. Non crei istanze della classe [TextPath](../../com.aspose.words/textpath/) direttamente.

 **Examples:** 

Mostra come lavorare con WordArt.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBold()](#getBold) | True se il carattere è formattato in grassetto. |
| [getFitPath()](#getFitPath) | Definisce se il testo si adatta al percorso di una forma. |
| [getFitShape()](#getFitShape) | Definisce se il testo si adatta al riquadro di delimitazione di una forma. |
| [getFontFamily()](#getFontFamily) | Definisce la famiglia del carattere del percorso di testo. |
| [getItalic()](#getItalic) | Vero se il carattere è formattato in corsivo. |
| [getKerning()](#getKerning) | Determina se la spaziatura dei caratteri (kerning) è attivata. |
| [getOn()](#getOn) | Definisce se il testo è visualizzato. |
| [getReverseRows()](#getReverseRows) | Determina se l'ordine di disposizione delle righe è invertito. |
| [getRotateLetters()](#getRotateLetters) | Determina se le lettere del testo sono ruotate. |
| [getSameLetterHeights()](#getSameLetterHeights) | Determina se tutte le lettere avranno la stessa altezza indipendentemente dal caso iniziale. |
| [getShadow()](#getShadow) | Definisce se un'ombra è applicata al testo su un percorso di testo. |
| [getSize()](#getSize) | Definisce la dimensione del carattere in punti. |
| [getSmallCaps()](#getSmallCaps) | Vero se il carattere è formattato in lettere maiuscole piccole. |
| [getSpacing()](#getSpacing) | Definisce la quantità di spaziatura per il testo. |
| [getStrikeThrough()](#getStrikeThrough) | Vero se il carattere è formattato con barrato. |
| [getText()](#getText) | Definisce il testo del percorso di testo. |
| [getTextPathAlignment()](#getTextPathAlignment) | Definisce l'allineamento del testo. |
| [getTrim()](#getTrim) | Determina se lo spazio extra è rimosso sopra e sotto il testo. |
| [getUnderline()](#getUnderline) | Vero se il carattere è sottolineato. |
| [getXScale()](#getXScale) | Determina se verrà usato un percorso di testo rettilineo invece del percorso della forma. |
| [setBold(boolean value)](#setBold-boolean) | True se il carattere è formattato in grassetto. |
| [setFitPath(boolean value)](#setFitPath-boolean) | Definisce se il testo si adatta al percorso di una forma. |
| [setFitShape(boolean value)](#setFitShape-boolean) | Definisce se il testo si adatta al riquadro di delimitazione di una forma. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Definisce la famiglia del carattere del percorso di testo. |
| [setItalic(boolean value)](#setItalic-boolean) | Vero se il carattere è formattato in corsivo. |
| [setKerning(boolean value)](#setKerning-boolean) | Determina se la spaziatura dei caratteri (kerning) è attivata. |
| [setOn(boolean value)](#setOn-boolean) | Definisce se il testo è visualizzato. |
| [setReverseRows(boolean value)](#setReverseRows-boolean) | Determina se l'ordine di disposizione delle righe è invertito. |
| [setRotateLetters(boolean value)](#setRotateLetters-boolean) | Determina se le lettere del testo sono ruotate. |
| [setSameLetterHeights(boolean value)](#setSameLetterHeights-boolean) | Determina se tutte le lettere avranno la stessa altezza indipendentemente dal caso iniziale. |
| [setShadow(boolean value)](#setShadow-boolean) | Definisce se un'ombra è applicata al testo su un percorso di testo. |
| [setSize(double value)](#setSize-double) | Definisce la dimensione del carattere in punti. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | Vero se il carattere è formattato in lettere maiuscole piccole. |
| [setSpacing(double value)](#setSpacing-double) | Definisce la quantità di spaziatura per il testo. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | Vero se il carattere è formattato con barrato. |
| [setText(String value)](#setText-java.lang.String) | Definisce il testo del percorso di testo. |
| [setTextPathAlignment(int value)](#setTextPathAlignment-int) | Definisce l'allineamento del testo. |
| [setTrim(boolean value)](#setTrim-boolean) | Determina se lo spazio extra è rimosso sopra e sotto il testo. |
| [setUnderline(boolean value)](#setUnderline-boolean) | Vero se il carattere è sottolineato. |
| [setXScale(boolean value)](#setXScale-boolean) | Determina se verrà usato un percorso di testo rettilineo invece del percorso della forma. |
### getBold() {#getBold}
```
public boolean getBold()
```


True se il carattere è formattato in grassetto.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getFitPath() {#getFitPath}
```
public boolean getFitPath()
```


Definisce se il testo si adatta al percorso di una forma.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getFitShape() {#getFitShape}
```
public boolean getFitShape()
```


Definisce se il testo si adatta al riquadro di delimitazione di una forma.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Definisce la famiglia del carattere del percorso di testo.

 **Remarks:** 

Il valore predefinito è Arial.

 **Examples:** 

Mostra come lavorare con WordArt.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Vero se il carattere è formattato in corsivo.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getKerning() {#getKerning}
```
public boolean getKerning()
```


Determina se la spaziatura dei caratteri (kerning) è attivata.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getOn() {#getOn}
```
public boolean getOn()
```


Definisce se il testo è visualizzato.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getReverseRows() {#getReverseRows}
```
public boolean getReverseRows()
```


Determina se l'ordine di disposizione delle righe è invertito.

 **Remarks:** 

Il valore predefinito è  false .

Se vero, l'ordine di disposizione delle righe è invertito. Questo attributo è usato per il layout del testo verticale.

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getRotateLetters() {#getRotateLetters}
```
public boolean getRotateLetters()
```


Determina se le lettere del testo sono ruotate.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getSameLetterHeights() {#getSameLetterHeights}
```
public boolean getSameLetterHeights()
```


Determina se tutte le lettere avranno la stessa altezza indipendentemente dal caso iniziale.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Definisce se un'ombra è applicata al testo su un percorso di testo.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getSize() {#getSize}
```
public double getSize()
```


Definisce la dimensione del carattere in punti.

 **Remarks:** 

Il valore predefinito è 36.

 **Examples:** 

Mostra come lavorare con WordArt.

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
double - Il valore double corrispondente.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


Vero se il carattere è formattato in lettere maiuscole piccole.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Definisce la quantità di spaziatura per il testo. 1 significa 100%.

 **Remarks:** 

Il valore predefinito è 1.

 **Examples:** 

Mostra come lavorare con WordArt.

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
double - Il valore double corrispondente.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


Vero se il carattere è formattato con barrato.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getText() {#getText}
```
public String getText()
```


Definisce il testo del percorso di testo.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come lavorare con WordArt.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getTextPathAlignment() {#getTextPathAlignment}
```
public int getTextPathAlignment()
```


Definisce l'allineamento del testo.

 **Remarks:** 

Il valore predefinito è [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER).

 **Examples:** 

Mostra come lavorare con WordArt.

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
int - Il valore int corrispondente. Il valore restituito è uno dei costanti di [TextPathAlignment](../../com.aspose.words/textpathalignment/).
### getTrim() {#getTrim}
```
public boolean getTrim()
```


Determina se lo spazio extra è rimosso sopra e sotto il testo.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getUnderline() {#getUnderline}
```
public boolean getUnderline()
```


Vero se il carattere è sottolineato.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### getXScale() {#getXScale}
```
public boolean getXScale()
```


Determina se verrà usato un percorso di testo rettilineo invece del percorso della forma.

 **Remarks:** 

Il valore predefinito è  false .

Se true, il testo scorre lungo un percorso da sinistra a destra lungo il valore x del bordo inferiore della forma.

 **Examples:** 

Mostra come lavorare con WordArt.

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
boolean - Il valore booleano corrispondente.
### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True se il carattere è formattato in grassetto.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setFitPath(boolean value) {#setFitPath-boolean}
```
public void setFitPath(boolean value)
```


Definisce se il testo si adatta al percorso di una forma.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setFitShape(boolean value) {#setFitShape-boolean}
```
public void setFitShape(boolean value)
```


Definisce se il testo si adatta al riquadro di delimitazione di una forma.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Definisce la famiglia del carattere del percorso di testo.

 **Remarks:** 

Il valore predefinito è Arial.

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Vero se il carattere è formattato in corsivo.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setKerning(boolean value) {#setKerning-boolean}
```
public void setKerning(boolean value)
```


Determina se la spaziatura dei caratteri (kerning) è attivata.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```


Definisce se il testo è visualizzato.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setReverseRows(boolean value) {#setReverseRows-boolean}
```
public void setReverseRows(boolean value)
```


Determina se l'ordine di disposizione delle righe è invertito.

 **Remarks:** 

Il valore predefinito è  false .

Se vero, l'ordine di disposizione delle righe è invertito. Questo attributo è usato per il layout del testo verticale.

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setRotateLetters(boolean value) {#setRotateLetters-boolean}
```
public void setRotateLetters(boolean value)
```


Determina se le lettere del testo sono ruotate.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setSameLetterHeights(boolean value) {#setSameLetterHeights-boolean}
```
public void setSameLetterHeights(boolean value)
```


Determina se tutte le lettere avranno la stessa altezza indipendentemente dal caso iniziale.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Definisce se un'ombra è applicata al testo su un percorso di testo.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Definisce la dimensione del carattere in punti.

 **Remarks:** 

Il valore predefinito è 36.

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il valore double corrispondente. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


Vero se il carattere è formattato in lettere maiuscole piccole.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Definisce la quantità di spaziatura per il testo. 1 significa 100%.

 **Remarks:** 

Il valore predefinito è 1.

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il valore double corrispondente. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


Vero se il carattere è formattato con barrato.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Definisce il testo del percorso di testo.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setTextPathAlignment(int value) {#setTextPathAlignment-int}
```
public void setTextPathAlignment(int value)
```


Definisce l'allineamento del testo.

 **Remarks:** 

Il valore predefinito è [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER).

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere uno dei costanti di [TextPathAlignment](../../com.aspose.words/textpathalignment/). |

### setTrim(boolean value) {#setTrim-boolean}
```
public void setTrim(boolean value)
```


Determina se lo spazio extra è rimosso sopra e sotto il testo.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setUnderline(boolean value) {#setUnderline-boolean}
```
public void setUnderline(boolean value)
```


Vero se il carattere è sottolineato.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setXScale(boolean value) {#setXScale-boolean}
```
public void setXScale(boolean value)
```


Determina se verrà usato un percorso di testo rettilineo invece del percorso della forma.

 **Remarks:** 

Il valore predefinito è  false .

Se true, il testo scorre lungo un percorso da sinistra a destra lungo il valore x del bordo inferiore della forma.

 **Examples:** 

Mostra come lavorare con WordArt.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

