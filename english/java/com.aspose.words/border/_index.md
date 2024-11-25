---
title: Border
linktitle: Border
second_title: Aspose.Words for Java
description: Represents a border of an object in Java.
type: docs
weight: 45
url: /java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Represents a border of an object.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Remarks:** 

Borders can be applied to various document elements including paragraph, run of text inside a paragraph or a table cell.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Shows how to insert a paragraph with a top border.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Resets border properties to default values. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Determines whether the specified border is equal in value to the current border. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getColor()](#getColor) | Gets the border color. |
| [getDistanceFromText()](#getDistanceFromText) | Gets distance of the border from text or from the page edge in points. |
| [getLineStyle()](#getLineStyle) | Gets the border style. |
| [getLineWidth()](#getLineWidth) | Gets the border width in points. |
| [getShadow()](#getShadow) | Gets a value indicating whether the border has a shadow. |
| [getThemeColor()](#getThemeColor) | Gets the theme color in the applied color scheme that is associated with this Border object. |
| [getTintAndShade()](#getTintAndShade) | Gets a double value that lightens or darkens a color. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Returns  true  if the [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) is not [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE). |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the border color. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Sets distance of the border from text or from the page edge in points. |
| [setLineStyle(int value)](#setLineStyle-int) | Sets the border style. |
| [setLineWidth(double value)](#setLineWidth-double) | Sets the border width in points. |
| [setShadow(boolean value)](#setShadow-boolean) | Sets a value indicating whether the border has a shadow. |
| [setThemeColor(int value)](#setThemeColor-int) | Sets the theme color in the applied color scheme that is associated with this Border object. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Sets a double value that lightens or darkens a color. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Resets border properties to default values.

 **Remarks:** 

When border properties are reset to default values, the border is invisible.

 **Examples:** 

Shows how to remove borders from a paragraph.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

### equals(Border rhs) {#equals-com.aspose.words.Border}
```
public boolean equals(Border rhs)
```


Determines whether the specified border is equal in value to the current border.

 **Examples:** 

Shows how border collections can share elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

 **Examples:** 

Shows how border collections can share elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


Gets the border color.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
java.awt.Color - The border color.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Gets distance of the border from text or from the page edge in points.

 **Remarks:** 

Has no effect and will be automatically reset to zero for borders of table cells.

 **Examples:** 

Shows how to create a wide blue band border at the top of the first page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
double - Distance of the border from text or from the page edge in points.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Gets the border style.

 **Remarks:** 

If you set line style to none, then line width is automatically changed to zero.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
int - The border style. The returned value is one of [LineStyle](../../com.aspose.words/linestyle/) constants.
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Gets the border width in points.

 **Remarks:** 

If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
double - The border width in points.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Gets a value indicating whether the border has a shadow.

 **Remarks:** 

In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to  true .

 **Examples:** 

Shows how to create green wavy page border with a shadow.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Returns:**
boolean - A value indicating whether the border has a shadow.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Gets the theme color in the applied color scheme that is associated with this Border object.

 **Examples:** 

Shows how to insert a paragraph with a top border.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Returns:**
int - The theme color in the applied color scheme that is associated with this Border object. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Gets a double value that lightens or darkens a color.

**Returns:**
double - A double value that lightens or darkens a color.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Returns  true  if the [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) is not [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).

 **Examples:** 

Shows how to remove borders from a paragraph.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

**Returns:**
boolean -  true  if the [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) is not [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets the border color.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The border color. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Sets distance of the border from text or from the page edge in points.

 **Remarks:** 

Has no effect and will be automatically reset to zero for borders of table cells.

 **Examples:** 

Shows how to create a wide blue band border at the top of the first page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance of the border from text or from the page edge in points. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Sets the border style.

 **Remarks:** 

If you set line style to none, then line width is automatically changed to zero.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The border style. The value must be one of [LineStyle](../../com.aspose.words/linestyle/) constants. |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Sets the border width in points.

 **Remarks:** 

If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The border width in points. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Sets a value indicating whether the border has a shadow.

 **Remarks:** 

In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to  true .

 **Examples:** 

Shows how to create green wavy page border with a shadow.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the border has a shadow. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Sets the theme color in the applied color scheme that is associated with this Border object.

 **Examples:** 

Shows how to insert a paragraph with a top border.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The theme color in the applied color scheme that is associated with this Border object. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Sets a double value that lightens or darkens a color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens a color. |

