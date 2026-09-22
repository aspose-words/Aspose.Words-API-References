---
title: "TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words لـ Java"
description: "مجموعة من كائنات TextColumn تمثل جميع أعمدة النص في قسم من مستند في Java."
type: docs
weight: 671
url: /ar/java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

مجموعة من كائنات [TextColumn](../../com.aspose.words/textcolumn/) تمثل جميع أعمدة النص في قسم من مستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Sections ][Working with Sections].

 **Remarks:** 

استخدم [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int) لتعيين عدد أعمدة النص.

لجعل جميع الأعمدة ذات عرض متساوٍ ومباعدة بالتساوي، اضبط [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) إلى  true  وحدد مقدار المسافة بين الأعمدة في [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double). سيقوم MS Word بحساب عرض الأعمدة تلقائيًا.

إذا كان لديك [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) مضبوطًا على  false ، تحتاج إلى تحديد العرض والمسافة لكل عمود على حدة. استخدم الفهرس للوصول إلى كائنات [TextColumn](../../com.aspose.words/textcolumn/) الفردية.

عند استخدام عرض أعمدة مخصص، تأكد من أن مجموع جميع عروض الأعمدة والمسافات بينها يساوي عرض الصفحة ناقص هوامش الصفحة اليسرى واليمنى.

 **Examples:** 

يوضح كيفية إنشاء أعمدة متعددة متباعدة بالتساوي في قسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يعيد عمود نص في الفهرس المحدد. |
| [getCount()](#getCount) | يحصل على عدد الأعمدة في قسم المستند. |
| [getEvenlySpaced()](#getEvenlySpaced) | صحيح إذا كانت أعمدة النص ذات عرض متساوٍ ومباعدة بالتساوي. |
| [getLineBetween()](#getLineBetween) | عند  true ، يضيف خطًا عموديًا بين الأعمدة. |
| [getSpacing()](#getSpacing) | عند تباعد الأعمدة بالتساوي، يحصل أو يضبط مقدار المسافة بين كل عمود بالنقاط. |
| [getWidth()](#getWidth) | عند تباعد الأعمدة بالتساوي، يحصل على عرض الأعمدة. |
| [setCount(int newCount)](#setCount-int) | ينظم النص في عدد الأعمدة النصية المحدد. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | صحيح إذا كانت أعمدة النص ذات عرض متساوٍ ومباعدة بالتساوي. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | عند  true ، يضيف خطًا عموديًا بين الأعمدة. |
| [setSpacing(double value)](#setSpacing-double) | عند تباعد الأعمدة بالتساوي، يحصل أو يضبط مقدار المسافة بين كل عمود بالنقاط. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


يعيد عمود نص في الفهرس المحدد.

 **Examples:** 

يوضح كيفية إنشاء أعمدة غير متباعدة بالتساوي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد الأعمدة في قسم المستند.

 **Examples:** 

يوضح كيفية إنشاء أعمدة متعددة متباعدة بالتساوي في قسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
int - عدد الأعمدة في قسم المستند.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


صحيح إذا كانت أعمدة النص ذات عرض متساوٍ ومباعدة بالتساوي.

 **Examples:** 

يوضح كيفية إنشاء أعمدة غير متباعدة بالتساوي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


عند  true ، يضيف خطًا عموديًا بين الأعمدة.

 **Examples:** 

يوضح كيفية فصل الأعمدة بخط عمودي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


عند تباعد الأعمدة بالتساوي، يحصل أو يضبط مقدار المسافة بين كل عمود بالنقاط.

 **Remarks:** 

يؤثر فقط عندما يكون [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) مضبوطًا على  true .

 **Examples:** 

يوضح كيفية إنشاء أعمدة متعددة متباعدة بالتساوي في قسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - القيمة المقابلة للـ double.
### getWidth() {#getWidth}
```
public double getWidth()
```


عند تباعد الأعمدة بالتساوي، يحصل على عرض الأعمدة.

 **Remarks:** 

يؤثر فقط عندما يكون [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) مضبوطًا على  true .

 **Examples:** 

يوضح كيفية إنشاء أعمدة متعددة متباعدة بالتساوي في قسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - القيمة المقابلة للـ double.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


ينظم النص في عدد الأعمدة النصية المحدد.

 **Remarks:** 

عندما يكون [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) هو  false  وتزيد عدد الأعمدة، يتم إنشاء كائنات [TextColumn](../../com.aspose.words/textcolumn/) جديدة بعرض ومسافة صفر. تحتاج إلى ضبط العرض والمسافة للأعمدة الجديدة.

 **Examples:** 

يوضح كيفية إنشاء أعمدة متعددة متباعدة بالتساوي في قسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| newCount | int | عدد الأعمدة التي سيتم ترتيب النص فيها. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


صحيح إذا كانت أعمدة النص ذات عرض متساوٍ ومباعدة بالتساوي.

 **Examples:** 

يوضح كيفية إنشاء أعمدة غير متباعدة بالتساوي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


عند  true ، يضيف خطًا عموديًا بين الأعمدة.

 **Examples:** 

يوضح كيفية فصل الأعمدة بخط عمودي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


عند تباعد الأعمدة بالتساوي، يحصل أو يضبط مقدار المسافة بين كل عمود بالنقاط.

 **Remarks:** 

يؤثر فقط عندما يكون [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) مضبوطًا على  true .

 **Examples:** 

يوضح كيفية إنشاء أعمدة متعددة متباعدة بالتساوي في قسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

