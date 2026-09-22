---
title: "TextPath"
linktitle: "TextPath"
second_title: "Aspose.Words لـ Java"
description: "يحدد النص وتنسيق مسار النص لكائن WordArt في Java."
type: docs
weight: 676
url: /ar/java/com.aspose.words/textpath/
---

**Inheritance:**
java.lang.Object
```
public class TextPath
```

يعرف النص وتنسيق مسار النص (لكائن WordArt).

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Shapes ][Working with Shapes].

 **Remarks:** 

استخدم الخاصية [Shape.getTextPath()](../../com.aspose.words/shape/\#getTextPath) للوصول إلى خصائص WordArt لشكل. لا تقوم بإنشاء مثيلات من الفئة [TextPath](../../com.aspose.words/textpath/) مباشرةً.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBold()](#getBold) | صحيح إذا كان الخط مُنسقًا كغامق. |
| [getFitPath()](#getFitPath) | يحدد ما إذا كان النص يتناسب مع مسار الشكل. |
| [getFitShape()](#getFitShape) | يحدد ما إذا كان النص يتناسب مع صندوق الحدود للشكل. |
| [getFontFamily()](#getFontFamily) | يحدد عائلة خط مسار النص. |
| [getItalic()](#getItalic) | صحيح إذا كان الخط مُنسقًا كخط مائل. |
| [getKerning()](#getKerning) | يحدد ما إذا كان تعديل التباعد بين الحروف (kerning) مُفعَّلًا. |
| [getOn()](#getOn) | يحدد ما إذا كان النص معروضًا. |
| [getReverseRows()](#getReverseRows) | يحدد ما إذا كان ترتيب تخطيط الصفوف مقلوبًا. |
| [getRotateLetters()](#getRotateLetters) | يحدد ما إذا كانت حروف النص مُدوَّرة. |
| [getSameLetterHeights()](#getSameLetterHeights) | يحدد ما إذا كانت جميع الحروف ستكون بنفس الارتفاع بغض النظر عن الحالة الأولية. |
| [getShadow()](#getShadow) | يحدد ما إذا كان الظل يُطبق على النص في مسار النص. |
| [getSize()](#getSize) | يحدد حجم الخط بالنقاط. |
| [getSmallCaps()](#getSmallCaps) | صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية. |
| [getSpacing()](#getSpacing) | يحدد مقدار التباعد للنص. |
| [getStrikeThrough()](#getStrikeThrough) | صحيح إذا كان الخط مُنسقًا كنص مشطوب. |
| [getText()](#getText) | يحدد نص مسار النص. |
| [getTextPathAlignment()](#getTextPathAlignment) | يحدد محاذاة النص. |
| [getTrim()](#getTrim) | يحدد ما إذا كان يتم إزالة المسافة الزائدة فوق وأسفل النص. |
| [getUnderline()](#getUnderline) | صحيح إذا كان الخط مُسطَّرًا. |
| [getXScale()](#getXScale) | يحدد ما إذا كان سيتم استخدام مسار نص مستقيم بدلاً من مسار الشكل. |
| [setBold(boolean value)](#setBold-boolean) | صحيح إذا كان الخط مُنسقًا كغامق. |
| [setFitPath(boolean value)](#setFitPath-boolean) | يحدد ما إذا كان النص يتناسب مع مسار الشكل. |
| [setFitShape(boolean value)](#setFitShape-boolean) | يحدد ما إذا كان النص يتناسب مع صندوق الحدود للشكل. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | يحدد عائلة خط مسار النص. |
| [setItalic(boolean value)](#setItalic-boolean) | صحيح إذا كان الخط مُنسقًا كخط مائل. |
| [setKerning(boolean value)](#setKerning-boolean) | يحدد ما إذا كان تعديل التباعد بين الحروف (kerning) مُفعَّلًا. |
| [setOn(boolean value)](#setOn-boolean) | يحدد ما إذا كان النص معروضًا. |
| [setReverseRows(boolean value)](#setReverseRows-boolean) | يحدد ما إذا كان ترتيب تخطيط الصفوف مقلوبًا. |
| [setRotateLetters(boolean value)](#setRotateLetters-boolean) | يحدد ما إذا كانت حروف النص مُدوَّرة. |
| [setSameLetterHeights(boolean value)](#setSameLetterHeights-boolean) | يحدد ما إذا كانت جميع الحروف ستكون بنفس الارتفاع بغض النظر عن الحالة الأولية. |
| [setShadow(boolean value)](#setShadow-boolean) | يحدد ما إذا كان الظل يُطبق على النص في مسار النص. |
| [setSize(double value)](#setSize-double) | يحدد حجم الخط بالنقاط. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية. |
| [setSpacing(double value)](#setSpacing-double) | يحدد مقدار التباعد للنص. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | صحيح إذا كان الخط مُنسقًا كنص مشطوب. |
| [setText(String value)](#setText-java.lang.String) | يحدد نص مسار النص. |
| [setTextPathAlignment(int value)](#setTextPathAlignment-int) | يحدد محاذاة النص. |
| [setTrim(boolean value)](#setTrim-boolean) | يحدد ما إذا كان يتم إزالة المسافة الزائدة فوق وأسفل النص. |
| [setUnderline(boolean value)](#setUnderline-boolean) | صحيح إذا كان الخط مُسطَّرًا. |
| [setXScale(boolean value)](#setXScale-boolean) | يحدد ما إذا كان سيتم استخدام مسار نص مستقيم بدلاً من مسار الشكل. |
### getBold() {#getBold}
```
public boolean getBold()
```


صحيح إذا كان الخط مُنسقًا كغامق.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getFitPath() {#getFitPath}
```
public boolean getFitPath()
```


يحدد ما إذا كان النص يتناسب مع مسار الشكل.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getFitShape() {#getFitShape}
```
public boolean getFitShape()
```


يحدد ما إذا كان النص يتناسب مع صندوق الحدود للشكل.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


يحدد عائلة خط مسار النص.

 **Remarks:** 

القيمة الافتراضية هي Arial.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


صحيح إذا كان الخط مُنسقًا كخط مائل.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getKerning() {#getKerning}
```
public boolean getKerning()
```


يحدد ما إذا كان تعديل التباعد بين الحروف (kerning) مُفعَّلًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getOn() {#getOn}
```
public boolean getOn()
```


يحدد ما إذا كان النص معروضًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getReverseRows() {#getReverseRows}
```
public boolean getReverseRows()
```


يحدد ما إذا كان ترتيب تخطيط الصفوف مقلوبًا.

 **Remarks:** 

القيمة الافتراضية هي false.

إذا كان صحيحًا، يتم عكس ترتيب تخطيط الصفوف. تُستخدم هذه الخاصية لتخطيط النص العمودي.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getRotateLetters() {#getRotateLetters}
```
public boolean getRotateLetters()
```


يحدد ما إذا كانت حروف النص مُدوَّرة.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getSameLetterHeights() {#getSameLetterHeights}
```
public boolean getSameLetterHeights()
```


يحدد ما إذا كانت جميع الحروف ستكون بنفس الارتفاع بغض النظر عن الحالة الأولية.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


يحدد ما إذا كان الظل يُطبق على النص في مسار النص.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getSize() {#getSize}
```
public double getSize()
```


يحدد حجم الخط بالنقاط.

 **Remarks:** 

القيمة الافتراضية هي 36.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
double - القيمة المقابلة للـ double.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


يحدد مقدار التباعد للنص. 1 يعني 100٪.

 **Remarks:** 

القيمة الافتراضية هي 1.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
double - القيمة المقابلة للـ double.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


صحيح إذا كان الخط مُنسقًا كنص مشطوب.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getText() {#getText}
```
public String getText()
```


يحدد نص مسار النص.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getTextPathAlignment() {#getTextPathAlignment}
```
public int getTextPathAlignment()
```


يحدد محاذاة النص.

 **Remarks:** 

القيمة الافتراضية هي [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER).

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
int - القيمة الصحيحة المقابلة. القيمة المرجعة هي واحدة من ثوابت [TextPathAlignment](../../com.aspose.words/textpathalignment/).
### getTrim() {#getTrim}
```
public boolean getTrim()
```


يحدد ما إذا كان يتم إزالة المسافة الزائدة فوق وأسفل النص.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getUnderline() {#getUnderline}
```
public boolean getUnderline()
```


صحيح إذا كان الخط مُسطَّرًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### getXScale() {#getXScale}
```
public boolean getXScale()
```


يحدد ما إذا كان سيتم استخدام مسار نص مستقيم بدلاً من مسار الشكل.

 **Remarks:** 

القيمة الافتراضية هي false.

إذا كان true ، يتحرك النص على طول مسار من اليسار إلى اليمين على قيمة x للحد الأدنى للشكل.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
boolean - القيمة المنطقية المقابلة.
### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


صحيح إذا كان الخط مُنسقًا كغامق.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setFitPath(boolean value) {#setFitPath-boolean}
```
public void setFitPath(boolean value)
```


يحدد ما إذا كان النص يتناسب مع مسار الشكل.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setFitShape(boolean value) {#setFitShape-boolean}
```
public void setFitShape(boolean value)
```


يحدد ما إذا كان النص يتناسب مع صندوق الحدود للشكل.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


يحدد عائلة خط مسار النص.

 **Remarks:** 

القيمة الافتراضية هي Arial.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


صحيح إذا كان الخط مُنسقًا كخط مائل.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setKerning(boolean value) {#setKerning-boolean}
```
public void setKerning(boolean value)
```


يحدد ما إذا كان تعديل التباعد بين الحروف (kerning) مُفعَّلًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```


يحدد ما إذا كان النص معروضًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setReverseRows(boolean value) {#setReverseRows-boolean}
```
public void setReverseRows(boolean value)
```


يحدد ما إذا كان ترتيب تخطيط الصفوف مقلوبًا.

 **Remarks:** 

القيمة الافتراضية هي false.

إذا كان صحيحًا، يتم عكس ترتيب تخطيط الصفوف. تُستخدم هذه الخاصية لتخطيط النص العمودي.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setRotateLetters(boolean value) {#setRotateLetters-boolean}
```
public void setRotateLetters(boolean value)
```


يحدد ما إذا كانت حروف النص مُدوَّرة.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSameLetterHeights(boolean value) {#setSameLetterHeights-boolean}
```
public void setSameLetterHeights(boolean value)
```


يحدد ما إذا كانت جميع الحروف ستكون بنفس الارتفاع بغض النظر عن الحالة الأولية.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


يحدد ما إذا كان الظل يُطبق على النص في مسار النص.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


يحدد حجم الخط بالنقاط.

 **Remarks:** 

القيمة الافتراضية هي 36.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


صحيح إذا كان الخط مُنسقًا كحروف صغيرة رأسية.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


يحدد مقدار التباعد للنص. 1 يعني 100٪.

 **Remarks:** 

القيمة الافتراضية هي 1.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


صحيح إذا كان الخط مُنسقًا كنص مشطوب.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


يحدد نص مسار النص.

 **Remarks:** 

القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setTextPathAlignment(int value) {#setTextPathAlignment-int}
```
public void setTextPathAlignment(int value)
```


يحدد محاذاة النص.

 **Remarks:** 

القيمة الافتراضية هي [TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment/\#CENTER).

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة المقابلة. يجب أن تكون القيمة واحدة من ثوابت [TextPathAlignment](../../com.aspose.words/textpathalignment/). |

### setTrim(boolean value) {#setTrim-boolean}
```
public void setTrim(boolean value)
```


يحدد ما إذا كان يتم إزالة المسافة الزائدة فوق وأسفل النص.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUnderline(boolean value) {#setUnderline-boolean}
```
public void setUnderline(boolean value)
```


صحيح إذا كان الخط مُسطَّرًا.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setXScale(boolean value) {#setXScale-boolean}
```
public void setXScale(boolean value)
```


يحدد ما إذا كان سيتم استخدام مسار نص مستقيم بدلاً من مسار الشكل.

 **Remarks:** 

القيمة الافتراضية هي false.

إذا كان true ، يتحرك النص على طول مسار من اليسار إلى اليمين على قيمة x للحد الأدنى للشكل.

 **Examples:** 

يعرض كيفية العمل مع WordArt.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

