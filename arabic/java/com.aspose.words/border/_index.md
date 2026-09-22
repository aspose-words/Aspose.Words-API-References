---
title: "حد"
linktitle: "حد"
second_title: "Aspose.Words لـ Java"
description: "يمثل حدًا لكائن في Java."
type: docs
weight: 46
url: /ar/java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object، [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

يمثل حدًا لكائن.

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

يمكن تطبيق الحدود على عناصر مستند مختلفة بما في ذلك الفقرة، أو مجموعة نص داخل الفقرة، أو خلية جدول.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

يظهر كيفية إدراج فقرة بحد أعلى.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearFormatting()](#clearFormatting) | يعيد تعيين خصائص الحد إلى القيم الافتراضية. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | يحدد ما إذا كان الحد المحدد مساويًا في القيمة للحد الحالي. |
| [equals(Object obj)](#equals-java.lang.Object) | يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي. |
| [getColor()](#getColor) | يحصل على لون الحد. |
| [getDistanceFromText()](#getDistanceFromText) | يحصل على مسافة الحد من النص أو من حافة الصفحة بالنقاط. |
| [getLineStyle()](#getLineStyle) | يحصل على نمط الحد. |
| [getLineWidth()](#getLineWidth) | يحصل على عرض الحد بالنقاط. |
| [getShadow()](#getShadow) | يحصل على قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |
| [getThemeColor()](#getThemeColor) | يحصل على لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن Border. |
| [getTintAndShade()](#getTintAndShade) | يحصل على قيمة مزدوجة تُفتح أو تُغميق اللون. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | يرجع  true  إذا لم يكن [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) هو [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE). |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط لون الحد. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | يضبط مسافة الحد من النص أو من حافة الصفحة بالنقاط. |
| [setLineStyle(int value)](#setLineStyle-int) | يضبط نمط الحد. |
| [setLineWidth(double value)](#setLineWidth-double) | يضبط عرض الحد بالنقاط. |
| [setShadow(boolean value)](#setShadow-boolean) | يضبط قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |
| [setThemeColor(int value)](#setThemeColor-int) | يضبط لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن Border. |
| [setTintAndShade(double value)](#setTintAndShade-double) | يضبط قيمة مزدوجة تُفتح أو تُغميق اللون. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


يعيد تعيين خصائص الحد إلى القيم الافتراضية.

 **Remarks:** 

عند إعادة تعيين خصائص الحد إلى القيم الافتراضية، يصبح الحد غير مرئي.

 **Examples:** 

يوضح كيفية إزالة الحدود من فقرة.

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


يحدد ما إذا كان الحد المحدد مساويًا في القيمة للحد الحالي.

 **Examples:** 

يوضح كيف يمكن لمجموعات الحدود مشاركة العناصر.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي.

 **Examples:** 

يوضح كيف يمكن لمجموعات الحدود مشاركة العناصر.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


يحصل على لون الحد.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

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
java.awt.Color - لون الحد.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


يحصل على مسافة الحد من النص أو من حافة الصفحة بالنقاط.

 **Remarks:** 

ليس له أي تأثير وسيتم إعادة ضبطه تلقائيًا إلى الصفر للحدود في خلايا الجدول.

 **Examples:** 

يوضح كيفية إنشاء حد على شكل شريط أزرق عريض في أعلى الصفحة الأولى.

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
double - مسافة الحد من النص أو من حافة الصفحة بالنقاط.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


يحصل على نمط الحد.

 **Remarks:** 

إذا قمت بتعيين نمط الخط إلى none، فسيتم تغيير عرض الخط تلقائيًا إلى صفر.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

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
int - نمط الحد. القيمة المرجعة هي واحدة من ثوابت [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


يحصل على عرض الحد بالنقاط.

 **Remarks:** 

إذا قمت بتعيين عرض الخط أكبر من الصفر عندما يكون نمط الخط هو none، يتم تغيير نمط الخط تلقائيًا إلى خط واحد.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

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
double - عرض الحد بالنقاط.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


يحصل على قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.

 **Remarks:** 

في Microsoft Word، لكي يكون للحد ظل، يجب أن تكون الحدود على جميع الجوانب الأربعة (اليسار، الأعلى، اليمين والأسفل) من نفس النوع والعرض واللون ويجب أن يكون خاصية Shadow مضبوطة على  true .

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
boolean - قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


يحصل على لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن Border.

 **Examples:** 

يظهر كيفية إدراج فقرة بحد أعلى.

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
int - لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن Border. القيمة المرجعة هي واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/).
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


يحصل على قيمة مزدوجة تُفتح أو تُغميق اللون.

**Returns:**
double - قيمة مزدوجة تُفتح أو تُغميق اللون.
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


يرجع  true  إذا لم يكن [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) هو [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).

 **Examples:** 

يوضح كيفية إزالة الحدود من فقرة.

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
boolean -  true  إذا لم يكن [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) هو [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


يضبط لون الحد.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون الحد. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


يضبط مسافة الحد من النص أو من حافة الصفحة بالنقاط.

 **Remarks:** 

ليس له أي تأثير وسيتم إعادة ضبطه تلقائيًا إلى الصفر للحدود في خلايا الجدول.

 **Examples:** 

يوضح كيفية إنشاء حد على شكل شريط أزرق عريض في أعلى الصفحة الأولى.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | مسافة الحد من النص أو من حافة الصفحة بالنقاط. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


يضبط نمط الحد.

 **Remarks:** 

إذا قمت بتعيين نمط الخط إلى none، فسيتم تغيير عرض الخط تلقائيًا إلى صفر.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | نمط الحد. يجب أن تكون القيمة واحدة من ثوابت [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


يضبط عرض الحد بالنقاط.

 **Remarks:** 

إذا قمت بتعيين عرض الخط أكبر من الصفر عندما يكون نمط الخط هو none، يتم تغيير نمط الخط تلقائيًا إلى خط واحد.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | عرض الحد بالنقاط. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.

 **Remarks:** 

في Microsoft Word، لكي يكون للحد ظل، يجب أن تكون الحدود على جميع الجوانب الأربعة (اليسار، الأعلى، اليمين والأسفل) من نفس النوع والعرض واللون ويجب أن يكون خاصية Shadow مضبوطة على  true .

 **Examples:** 

يوضح كيفية إنشاء حد صفحة متموج أخضر مع ظل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


يضبط لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن Border.

 **Examples:** 

يظهر كيفية إدراج فقرة بحد أعلى.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن Border. يجب أن تكون القيمة واحدة من ثوابت [ThemeColor](../../com.aspose.words/themecolor/). |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


يضبط قيمة مزدوجة تُفتح أو تُغميق اللون.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تُفتح أو تُغميق اللون. |

