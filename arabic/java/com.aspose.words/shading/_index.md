---
title: "التظليل"
linktitle: "التظليل"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على سمات التظليل لكائن في جافا."
type: docs
weight: 609
url: /ar/java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object، [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

يحتوي على خصائص التظليل لكائن.

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Examples:** 

يوضح كيفية تطبيق لون الحد والظل أثناء بناء جدول.

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

يوضح كيفية تزيين النص بالحدود والتظليل.

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


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearFormatting()](#clearFormatting) | يزيل التظليل من الكائن. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | يحدد ما إذا كان [Shading](../../com.aspose.words/shading/) المحدد مساويًا في القيمة إلى [Shading](../../com.aspose.words/shading/) الحالي. |
| [equals(Object obj)](#equals-java.lang.Object) | يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | يحصل على اللون المطبق على خلفية كائن [Shading](../../com.aspose.words/shading/). |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | يحصل على لون سمة نمط الخلفية في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/). |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | يحصل على قيمة مزدوجة تُفتح أو تُغلق لون سمة الخلفية. |
| [getForegroundPatternColor()](#getForegroundPatternColor) | يحصل على اللون المطبق على مقدمة كائن [Shading](../../com.aspose.words/shading/). |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | يحصل على لون سمة نمط المقدمة في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/). |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | يحصل على قيمة مزدوجة تُفتح أو تُغلق لون سمة المقدمة. |
| [getTexture()](#getTexture) | يحصل على نسيج التظليل. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | يضبط اللون المطبق على خلفية كائن [Shading](../../com.aspose.words/shading/). |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | يضبط لون سمة نمط الخلفية في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/). |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | يضبط قيمة مزدوجة تُفتح أو تُغلق لون سمة الخلفية. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | يضبط اللون المطبق على مقدمة كائن [Shading](../../com.aspose.words/shading/). |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | يضبط لون سمة نمط المقدمة في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/). |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | يضبط قيمة مزدوجة تُفتح أو تُغلق لون سمة المقدمة. |
| [setTexture(int value)](#setTexture-int) | يضبط نسيج التظليل. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


يزيل التظليل من الكائن.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

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


يحدد ما إذا كان [Shading](../../com.aspose.words/shading/) المحدد مساويًا في القيمة إلى [Shading](../../com.aspose.words/shading/) الحالي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


يحصل على اللون المطبق على خلفية كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية تزيين النص بالحدود والتظليل.

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
java.awt.Color - اللون المطبق على خلفية كائن [Shading](../../com.aspose.words/shading/).
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


يحصل على لون سمة نمط الخلفية في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية ضبط ألوان المقدمة والخلفية لنسيج التظليل.

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
int - لون سمة نمط الخلفية في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/). القيمة المرجعة هي واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/).
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


يحصل على قيمة مزدوجة تُفتح أو تُغلق لون سمة الخلفية.

**Returns:**
double - قيمة مزدوجة تُفتح أو تُغلق لون سمة الخلفية.
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


يحصل على اللون المطبق على مقدمة كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية تزيين النص بالحدود والتظليل.

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
java.awt.Color - اللون المطبق على مقدمة كائن [Shading](../../com.aspose.words/shading/).
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


يحصل على لون سمة نمط المقدمة في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية ضبط ألوان المقدمة والخلفية لنسيج التظليل.

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
int - لون سمة نمط المقدمة في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/). القيمة المرجعة هي واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/).
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


يحصل على قيمة مزدوجة تُفتح أو تُغلق لون سمة المقدمة.

**Returns:**
double - قيمة مزدوجة تُفتح أو تُغمق لون سمة المقدمة.
### getTexture() {#getTexture}
```
public int getTexture()
```


يحصل على نسيج التظليل.

 **Examples:** 

يوضح كيفية تزيين النص بالحدود والتظليل.

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
int - نسيج التظليل. القيمة المرجعة هي واحدة من ثوابت [TextureIndex](../../com.aspose.words/textureindex/).
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


يضبط اللون المطبق على خلفية كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية تزيين النص بالحدود والتظليل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.awt.Color | اللون المطبق على خلفية كائن [Shading](../../com.aspose.words/shading/). |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


يضبط لون سمة نمط الخلفية في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية ضبط ألوان المقدمة والخلفية لنسيج التظليل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | لون سمة نمط الخلفية في نظام الألوان المطبق المرتبط بهذا الكائن [Shading](../../com.aspose.words/shading/). يجب أن تكون القيمة واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


يضبط قيمة مزدوجة تُفتح أو تُغلق لون سمة الخلفية.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تُفتح أو تُغمق لون سمة الخلفية. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


يضبط اللون المطبق على مقدمة كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية تزيين النص بالحدود والتظليل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.awt.Color | اللون المطبق على مقدمة كائن [Shading](../../com.aspose.words/shading/). |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


يضبط لون سمة نمط المقدمة في نظام الألوان المطبق المرتبط بهذا كائن [Shading](../../com.aspose.words/shading/).

 **Examples:** 

يوضح كيفية ضبط ألوان المقدمة والخلفية لنسيج التظليل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | لون سمة نمط المقدمة في نظام الألوان المطبق المرتبط بهذا الكائن [Shading](../../com.aspose.words/shading/). يجب أن تكون القيمة واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/). |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


يضبط قيمة مزدوجة تُفتح أو تُغلق لون سمة المقدمة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تُفتح أو تُغمق لون سمة المقدمة. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


يضبط نسيج التظليل.

 **Examples:** 

يوضح كيفية تزيين النص بالحدود والتظليل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | نسيج التظليل. يجب أن تكون القيمة واحدة من ثوابت [TextureIndex](../../com.aspose.words/textureindex/). |

