---
title: "TextColumn"
linktitle: "TextColumn"
second_title: "Aspose.Words لـ Java"
description: "يمثل عمود نصي واحد في Java."
type: docs
weight: 670
url: /ar/java/com.aspose.words/textcolumn/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

يمثل عمود نصي واحد. [TextColumn](../../com.aspose.words/textcolumn/) هو عضو في مجموعة [TextColumnCollection](../../com.aspose.words/textcolumncollection/). مجموعة [TextColumn](../../com.aspose.words/textcolumn/) تشمل جميع الأعمدة في قسم من المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Sections ][Working with Sections].

 **Remarks:** 

[TextColumn](../../com.aspose.words/textcolumn/) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns. [TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) to  true .

عند إنشاء [TextColumn](../../com.aspose.words/textcolumn/) جديد يتم ضبط عرضه والمسافة بينه إلى الصفر.

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


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getSpaceAfter()](#getSpaceAfter) | يحصل على المسافة بين هذا العمود والعمود التالي بالنقاط. |
| [getWidth()](#getWidth) | يحصل على عرض عمود النص بالنقاط. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | يضبط المسافة بين هذا العمود والعمود التالي بالنقاط. |
| [setWidth(double value)](#setWidth-double) | يضبط عرض عمود النص بالنقاط. |
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


يحصل على المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير.

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
double - المسافة بين هذا العمود والعمود التالي بالنقاط.
### getWidth() {#getWidth}
```
public double getWidth()
```


يحصل على عرض عمود النص بالنقاط.

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
double - عرض عمود النص بالنقاط.
### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


يضبط المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير.

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
| قيمة | double | المسافة بين هذا العمود والعمود التالي بالنقاط. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


يضبط عرض عمود النص بالنقاط.

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
| قيمة | double | عرض عمود النص بالنقاط. |

