---
title: TextColumnCollection
linktitle: TextColumnCollection
second_title: Aspose.Words for Java
description: A collection of TextColumn objects that represent all the columns of text in a section of a document in Java.
type: docs
weight: 624
url: /java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

A collection of [TextColumn](../../com.aspose.words/textcolumn/) objects that represent all the columns of text in a section of a document.

To learn more, visit the [ Working with Sections ][Working with Sections] documentation article.

 **Remarks:** 

Use [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int) to set the number of text columns.

To make all columns equal width and spaced evenly, set [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) to  true  and specify the amount of space between the columns in [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double). MS Word will automatically calculate column widths.

If you have [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) set to  false , you need to specify width and spacing for each column individually. Use the indexer to access individual [TextColumn](../../com.aspose.words/textcolumn/) objects.

When using custom column widths, make sure the sum of all column widths and spacings between them equals page width minus left and right page margins.

 **Examples:** 

Shows how to create multiple evenly spaced columns in a section.

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
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Returns a text column at the specified index. |
| [getCount()](#getCount) | Gets the number of columns in the section of a document. |
| [getEvenlySpaced()](#getEvenlySpaced) | True if text columns are of equal width and evenly spaced. |
| [getLineBetween()](#getLineBetween) | When  true , adds a vertical line between columns. |
| [getSpacing()](#getSpacing) | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
| [getWidth()](#getWidth) | When columns are evenly spaced, gets the width of the columns. |
| [setCount(int newCount)](#setCount-int) | Arranges text into the specified number of text columns. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | True if text columns are of equal width and evenly spaced. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | When  true , adds a vertical line between columns. |
| [setSpacing(double value)](#setSpacing-double) | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


Returns a text column at the specified index.

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
| index | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of columns in the section of a document.

 **Examples:** 

Shows how to create multiple evenly spaced columns in a section.

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
int - The number of columns in the section of a document.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


True if text columns are of equal width and evenly spaced.

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
boolean - The corresponding  boolean  value.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


When  true , adds a vertical line between columns.

 **Examples:** 

Shows how to separate columns with a vertical line.

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
boolean - The corresponding  boolean  value.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


When columns are evenly spaced, gets or sets the amount of space between each column in points.

 **Remarks:** 

Has effect only when [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) is set to  true .

 **Examples:** 

Shows how to create multiple evenly spaced columns in a section.

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
double - The corresponding  double  value.
### getWidth() {#getWidth}
```
public double getWidth()
```


When columns are evenly spaced, gets the width of the columns.

 **Remarks:** 

Has effect only when [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) is set to  true .

 **Examples:** 

Shows how to create multiple evenly spaced columns in a section.

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
double - The corresponding  double  value.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


Arranges text into the specified number of text columns.

 **Remarks:** 

When [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) is  false  and you increase the number of columns, new [TextColumn](../../com.aspose.words/textcolumn/) objects are created with zero width and spacing. You need to set width and spacing for the new columns.

 **Examples:** 

Shows how to create multiple evenly spaced columns in a section.

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
| Parameter | Type | Description |
| --- | --- | --- |
| newCount | int | The number of columns the text is to be arranged into. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


True if text columns are of equal width and evenly spaced.

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
| value | boolean | The corresponding  boolean  value. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


When  true , adds a vertical line between columns.

 **Examples:** 

Shows how to separate columns with a vertical line.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


When columns are evenly spaced, gets or sets the amount of space between each column in points.

 **Remarks:** 

Has effect only when [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) is set to  true .

 **Examples:** 

Shows how to create multiple evenly spaced columns in a section.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

