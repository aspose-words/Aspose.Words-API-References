---
title: TextColumn
linktitle: TextColumn
second_title: Aspose.Words for Java
description: Represents a single text column in Java.
type: docs
weight: 644
url: /java/com.aspose.words/textcolumn/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

Represents a single text column. [TextColumn](../../com.aspose.words/textcolumn/) is a member of the [TextColumnCollection](../../com.aspose.words/textcolumncollection/) collection. The [TextColumn](../../com.aspose.words/textcolumn/) collection includes all the columns in a section of a document.

To learn more, visit the [ Working with Sections ][Working with Sections] documentation article.

 **Remarks:** 

[TextColumn](../../com.aspose.words/textcolumn/) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns. [TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) to  true .

When a new [TextColumn](../../com.aspose.words/textcolumn/) is created it has its width and spacing set to zero.

 **Examples:** 

Shows how to create unevenly spaced columns.

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
## Methods

| Method | Description |
| --- | --- |
| [getSpaceAfter()](#getSpaceAfter) | Gets the space between this column and the next column in points. |
| [getWidth()](#getWidth) | Gets the width of the text column in points. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Sets the space between this column and the next column in points. |
| [setWidth(double value)](#setWidth-double) | Sets the width of the text column in points. |
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Gets the space between this column and the next column in points. Not required for the last column.

 **Examples:** 

Shows how to create unevenly spaced columns.

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
double - The space between this column and the next column in points.
### getWidth() {#getWidth}
```
public double getWidth()
```


Gets the width of the text column in points.

 **Examples:** 

Shows how to create unevenly spaced columns.

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
double - The width of the text column in points.
### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Sets the space between this column and the next column in points. Not required for the last column.

 **Examples:** 

Shows how to create unevenly spaced columns.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The space between this column and the next column in points. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Sets the width of the text column in points.

 **Examples:** 

Shows how to create unevenly spaced columns.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The width of the text column in points. |

