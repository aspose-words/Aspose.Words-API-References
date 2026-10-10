---
title: "TextPathAlignment"
linktitle: "TextPathAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da WordArt hizalaması."
type: docs
weight: 677
url: /tr/java/com.aspose.words/textpathalignment/
---

**Inheritance:**
java.lang.Object
```
public class TextPathAlignment
```

WordArt hizalaması.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CENTER](#CENTER) | Metni genişliğe ortala. |
| [LEFT](#LEFT) | Sola hizala. |
| [LETTER_JUSTIFY](#LETTER-JUSTIFY) | Genişliğe sığacak şekilde harfleri yay. |
| [RIGHT](#RIGHT) | Sağa hizala. |
| [STRETCH](#STRETCH) | Metnin her satırını genişliğe sığacak şekilde uzat. |
| [WORD_JUSTIFY](#WORD-JUSTIFY) | Genişliğe sığacak şekilde kelimeleri yay. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textPathAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int textPathAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textPathAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Metni genişliğe ortala.

### LEFT {#LEFT}
```
public static int LEFT
```


Sola hizala.

### LETTER_JUSTIFY {#LETTER-JUSTIFY}
```
public static int LETTER_JUSTIFY
```


Genişliğe sığacak şekilde harfleri yay.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Sağa hizala.

### STRETCH {#STRETCH}
```
public static int STRETCH
```


Metnin her satırını genişliğe sığacak şekilde uzat.

### WORD_JUSTIFY {#WORD-JUSTIFY}
```
public static int WORD_JUSTIFY
```


Genişliğe sığacak şekilde kelimeleri yay.

### length {#length}
```
public static int length
```


### fromName(String textPathAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String textPathAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textPathAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int textPathAlignment) {#getName-int}
```
public static String getName(int textPathAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textPathAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textPathAlignment) {#toString-int}
```
public static String toString(int textPathAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textPathAlignment | int |  |

**Returns:**
java.lang.String
