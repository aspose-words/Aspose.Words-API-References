---
title: "TextPath"
linktitle: "TextPath"
second_title: "Aspose.Words Java için"
description: "Java'da bir WordArt nesnesinin metin yolu için metni ve biçimlendirmeyi tanımlar."
type: docs
weight: 676
url: /tr/java/com.aspose.words/textpath/
---

**Inheritance:**
java.lang.Object
```
public class TextPath
```

Metin yolunun (WordArt nesnesi) metnini ve biçimlendirmesini tanımlar.

Daha fazla bilgi edinmek için [ Working with Shapes ][Working with Shapes] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir şeklin WordArt özelliklerine erişmek için [Shape.getTextPath()](../../com.aspose.words/shape/\#getTextPath) özelliğini kullanın. [TextPath](../../com.aspose.words/textpath/) sınıfının örneklerini doğrudan oluşturmazsınız.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBold()](#getBold) | Yazı tipi kalın olarak biçimlendirilmişse True. |
| [getFitPath()](#getFitPath) | Metnin bir şeklin yoluna uyup uymadığını tanımlar. |
| [getFitShape()](#getFitShape) | Metnin bir şeklin sınırlayıcı kutusuna sığıp sığmadığını tanımlar. |
| [getFontFamily()](#getFontFamily) | Metin yolu yazı tipinin ailesini tanımlar. |
| [getItalic()](#getItalic) | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [getKerning()](#getKerning) | Kerning'in açık olup olmadığını belirler. |
| [getOn()](#getOn) | Metnin görüntülenip görüntülenmediğini tanımlar. |
| [getReverseRows()](#getReverseRows) | Satırların yerleşim sırasının ters olup olmadığını belirler. |
| [getRotateLetters()](#getRotateLetters) | Metnin harflerinin döndürülüp döndürülmediğini belirler. |
| [getSameLetterHeights()](#getSameLetterHeights) | Tüm harflerin başlangıç durumuna bakılmaksızın aynı yükseklikte olup olmayacağını belirler. |
| [getShadow()](#getShadow) | Metin yolundaki metne gölge uygulanıp uygulanmadığını tanımlar. |
| [getSize()](#getSize) | Yazı tipinin punto cinsinden boyutunu tanımlar. |
| [getSmallCaps()](#getSmallCaps) | Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur. |
| [getSpacing()](#getSpacing) | Metin için boşluk miktarını tanımlar. |
| [getStrikeThrough()](#getStrikeThrough) | Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur. |
| [getText()](#getText) | Metin yolunun metnini tanımlar. |
| [getTextPathAlignment()](#getTextPathAlignment) | Metnin hizalamasını tanımlar. |
| [getTrim()](#getTrim) | Metnin üstündeki ve altındaki ekstra boşluğun kaldırılıp kaldırılmadığını belirler. |
| [getUnderline()](#getUnderline) | Yazı tipi altı çizili ise doğrudur. |
| [getXScale()](#getXScale) | Şekil yolunun yerine düz bir metin yolunun kullanılıp kullanılmayacağını belirler. |
| [setBold(boolean value)](#setBold-boolean) | Yazı tipi kalın olarak biçimlendirilmişse True. |
| [setFitPath(boolean value)](#setFitPath-boolean) | Metnin bir şeklin yoluna uyup uymadığını tanımlar. |
| [setFitShape(boolean value)](#setFitShape-boolean) | Metnin bir şeklin sınırlayıcı kutusuna sığıp sığmadığını tanımlar. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Metin yolu yazı tipinin ailesini tanımlar. |
| [setItalic(boolean value)](#setItalic-boolean) | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [setKerning(boolean value)](#setKerning-boolean) | Kerning'in açık olup olmadığını belirler. |
| [setOn(boolean value)](#setOn-boolean) | Metnin görüntülenip görüntülenmediğini tanımlar. |
| [setReverseRows(boolean value)](#setReverseRows-boolean) | Satırların yerleşim sırasının ters olup olmadığını belirler. |
| [setRotateLetters(boolean value)](#setRotateLetters-boolean) | Metnin harflerinin döndürülüp döndürülmediğini belirler. |
| [setSameLetterHeights(boolean value)](#setSameLetterHeights-boolean) | Tüm harflerin başlangıç durumuna bakılmaksızın aynı yükseklikte olup olmayacağını belirler. |
| [setShadow(boolean value)](#setShadow-boolean) | Metin yolundaki metne gölge uygulanıp uygulanmadığını tanımlar. |
| [setSize(double value)](#setSize-double) | Yazı tipinin punto cinsinden boyutunu tanımlar. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur. |
| [setSpacing(double value)](#setSpacing-double) | Metin için boşluk miktarını tanımlar. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur. |
| [setText(String value)](#setText-java.lang.String) | Metin yolunun metnini tanımlar. |
| [setTextPathAlignment(int value)](#setTextPathAlignment-int) | Metnin hizalamasını tanımlar. |
| [setTrim(boolean value)](#setTrim-boolean) | Metnin üstündeki ve altındaki ekstra boşluğun kaldırılıp kaldırılmadığını belirler. |
| [setUnderline(boolean value)](#setUnderline-boolean) | Yazı tipi altı çizili ise doğrudur. |
| [setXScale(boolean value)](#setXScale-boolean) | Şekil yolunun yerine düz bir metin yolunun kullanılıp kullanılmayacağını belirler. |
### getBold() {#getBold}
```
public boolean getBold()
```


Yazı tipi kalın olarak biçimlendirilmişse True.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getFitPath() {#getFitPath}
```
public boolean getFitPath()
```


Metnin bir şeklin yoluna uyup uymadığını tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getFitShape() {#getFitShape}
```
public boolean getFitShape()
```


Metnin bir şeklin sınırlayıcı kutusuna sığıp sığmadığını tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Metin yolu yazı tipinin ailesini tanımlar.

 **Remarks:** 

Varsayılan değer Arial'dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Yazı tipi italik olarak biçimlendirilmişse doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getKerning() {#getKerning}
```
public boolean getKerning()
```


Kerning'in açık olup olmadığını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getOn() {#getOn}
```
public boolean getOn()
```


Metnin görüntülenip görüntülenmediğini tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getReverseRows() {#getReverseRows}
```
public boolean getReverseRows()
```


Satırların yerleşim sırasının ters olup olmadığını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

Eğer true ise, satırların yerleşim sırası ters olur. Bu öznitelik dikey metin yerleşimi için kullanılır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getRotateLetters() {#getRotateLetters}
```
public boolean getRotateLetters()
```


Metnin harflerinin döndürülüp döndürülmediğini belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getSameLetterHeights() {#getSameLetterHeights}
```
public boolean getSameLetterHeights()
```


Tüm harflerin başlangıç durumuna bakılmaksızın aynı yükseklikte olup olmayacağını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Metin yolundaki metne gölge uygulanıp uygulanmadığını tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getSize() {#getSize}
```
public double getSize()
```


Yazı tipinin punto cinsinden boyutunu tanımlar.

 **Remarks:** 

Varsayılan değer 36'dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
double - İlgili  double  değeri.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Metin için boşluk miktarını tanımlar. 1, %100 anlamına gelir.

 **Remarks:** 

Varsayılan değer 1'dir.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
double - İlgili  double  değeri.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getText() {#getText}
```
public String getText()
```


Metin yolunun metnini tanımlar.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
### getTextPathAlignment() {#getTextPathAlignment}
```
public int getTextPathAlignment()
```


Metnin hizalamasını tanımlar.

 **Remarks:** 

Varsayılan değer [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER)'dir.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
int - İlgili  int  değeri. Döndürülen değer, [TextPathAlignment](../../com.aspose.words/textpathalignment/) sabitlerinden biridir.
### getTrim() {#getTrim}
```
public boolean getTrim()
```


Metnin üstündeki ve altındaki ekstra boşluğun kaldırılıp kaldırılmadığını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getUnderline() {#getUnderline}
```
public boolean getUnderline()
```


Yazı tipi altı çizili ise doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getXScale() {#getXScale}
```
public boolean getXScale()
```


Şekil yolunun yerine düz bir metin yolunun kullanılıp kullanılmayacağını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

Eğer  true  ise, metin şeklin alt sınırının x değeri boyunca soldan sağa bir yol izler.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


Yazı tipi kalın olarak biçimlendirilmişse True.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setFitPath(boolean value) {#setFitPath-boolean}
```
public void setFitPath(boolean value)
```


Metnin bir şeklin yoluna uyup uymadığını tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setFitShape(boolean value) {#setFitShape-boolean}
```
public void setFitShape(boolean value)
```


Metnin bir şeklin sınırlayıcı kutusuna sığıp sığmadığını tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Metin yolu yazı tipinin ailesini tanımlar.

 **Remarks:** 

Varsayılan değer Arial'dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Yazı tipi italik olarak biçimlendirilmişse doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setKerning(boolean value) {#setKerning-boolean}
```
public void setKerning(boolean value)
```


Kerning'in açık olup olmadığını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```


Metnin görüntülenip görüntülenmediğini tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setReverseRows(boolean value) {#setReverseRows-boolean}
```
public void setReverseRows(boolean value)
```


Satırların yerleşim sırasının ters olup olmadığını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

Eğer true ise, satırların yerleşim sırası ters olur. Bu öznitelik dikey metin yerleşimi için kullanılır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setRotateLetters(boolean value) {#setRotateLetters-boolean}
```
public void setRotateLetters(boolean value)
```


Metnin harflerinin döndürülüp döndürülmediğini belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSameLetterHeights(boolean value) {#setSameLetterHeights-boolean}
```
public void setSameLetterHeights(boolean value)
```


Tüm harflerin başlangıç durumuna bakılmaksızın aynı yükseklikte olup olmayacağını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Metin yolundaki metne gölge uygulanıp uygulanmadığını tanımlar.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Yazı tipinin punto cinsinden boyutunu tanımlar.

 **Remarks:** 

Varsayılan değer 36'dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Metin için boşluk miktarını tanımlar. 1, %100 anlamına gelir.

 **Remarks:** 

Varsayılan değer 1'dir.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Metin yolunun metnini tanımlar.

 **Remarks:** 

Varsayılan değer boş bir dizedir.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setTextPathAlignment(int value) {#setTextPathAlignment-int}
```
public void setTextPathAlignment(int value)
```


Metnin hizalamasını tanımlar.

 **Remarks:** 

Varsayılan değer [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER)'dir.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [TextPathAlignment](../../com.aspose.words/textpathalignment/) sabitlerinden biri olmalıdır. |

### setTrim(boolean value) {#setTrim-boolean}
```
public void setTrim(boolean value)
```


Metnin üstündeki ve altındaki ekstra boşluğun kaldırılıp kaldırılmadığını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setUnderline(boolean value) {#setUnderline-boolean}
```
public void setUnderline(boolean value)
```


Yazı tipi altı çizili ise doğrudur.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setXScale(boolean value) {#setXScale-boolean}
```
public void setXScale(boolean value)
```


Şekil yolunun yerine düz bir metin yolunun kullanılıp kullanılmayacağını belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

Eğer  true  ise, metin şeklin alt sınırının x değeri boyunca soldan sağa bir yol izler.

 **Examples:** 

WordArt ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

