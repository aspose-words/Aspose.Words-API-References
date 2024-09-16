---
title: Shading
linktitle: Shading
second_title: Aspose.Words for Java
description: Contains shading attributes for an object in Java.
type: docs
weight: 568
url: /java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

Contains shading attributes for an object.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Examples:** 

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

Shows how to apply border and shading color while building a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start a table and set a default color/thickness for its borders.
 Table table = builder.startTable();
 table.setBorders(LineStyle.SINGLE, 2.0, Color.BLACK);

 // Create a row with two cells with different background colors.
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.RED);
 builder.writeln("Row 1, Cell 1.");
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Row 1, Cell 2.");
 builder.endRow();

 // Reset cell formatting to disable the background colors
 // set a custom border thickness for all new cells created by the builder,
 // then build a second row.
 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().getBorders().getLeft().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getRight().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getTop().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getBottom().setLineWidth(4.0);

 builder.insertCell();
 builder.writeln("Row 2, Cell 1.");
 builder.insertCell();
 builder.writeln("Row 2, Cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.TableBordersAndShading.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Removes shading from the object. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | Determines whether the specified [Shading](../../com.aspose.words/shading/) is equal in value to the current [Shading](../../com.aspose.words/shading/). |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | Gets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object. |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | Gets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | Gets a double value that lightens or darkens a background theme color. |
| [getForegroundPatternColor()](#getForegroundPatternColor) | Gets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object. |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | Gets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | Gets a double value that lightens or darkens a foreground theme color. |
| [getTexture()](#getTexture) | Gets the shading texture. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | Sets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object. |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | Sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | Sets a double value that lightens or darkens a background theme color. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | Sets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object. |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | Sets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | Sets a double value that lightens or darkens a foreground theme color. |
| [setTexture(int value)](#setTexture-int) | Sets the shading texture. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Removes shading from the object.

 **Examples:** 

Shows how to build a table with custom borders.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

### equals(Shading rhs) {#equals-com.aspose.words.Shading}
```
public boolean equals(Shading rhs)
```


Determines whether the specified [Shading](../../com.aspose.words/shading/) is equal in value to the current [Shading](../../com.aspose.words/shading/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


Gets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
java.awt.Color - The color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object.
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


Gets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to set foreground and background colors for shading texture.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Returns:**
int - The background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


Gets a double value that lightens or darkens a background theme color.

**Returns:**
double - A double value that lightens or darkens a background theme color.
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


Gets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
java.awt.Color - The color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object.
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


Gets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to set foreground and background colors for shading texture.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Returns:**
int - The foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


Gets a double value that lightens or darkens a foreground theme color.

**Returns:**
double - A double value that lightens or darkens a foreground theme color.
### getTexture() {#getTexture}
```
public int getTexture()
```


Gets the shading texture.

 **Examples:** 

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
int - The shading texture. The returned value is one of [TextureIndex](../../com.aspose.words/textureindex/) constants.
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
### setBackgroundPatternColor(Color value) {#setBackgroundPatternColor-java.awt.Color}
```
public void setBackgroundPatternColor(Color value)
```


Sets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object. |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


Sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to set foreground and background colors for shading texture.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


Sets a double value that lightens or darkens a background theme color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens a background theme color. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


Sets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object. |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


Sets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

 **Examples:** 

Shows how to set foreground and background colors for shading texture.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


Sets a double value that lightens or darkens a foreground theme color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens a foreground theme color. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


Sets the shading texture.

 **Examples:** 

Shows how to decorate text with borders and shading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The shading texture. The value must be one of [TextureIndex](../../com.aspose.words/textureindex/) constants. |

