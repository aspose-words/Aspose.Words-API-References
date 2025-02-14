---
title: MultiplePagesType
linktitle: MultiplePagesType
second_title: Aspose.Words for Java
description: Specifies how document is printed out in Java.
type: docs
weight: 460
url: /java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

Specifies how document is printed out.

 **Examples:** 

Shows how to configure a document that can be printed as a book fold.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | Specifies whether to print the document as a book fold. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | Specifies whether to print the document as a reverse book fold. |
| [DEFAULT](#DEFAULT) | Default value is [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | Swaps left and right margins on facing pages. |
| [NORMAL](#NORMAL) | Normal printing, no multiple pages specified. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | Prints two pages per sheet. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


Specifies whether to print the document as a book fold.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


Specifies whether to print the document as a reverse book fold.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value is [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


Swaps left and right margins on facing pages.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal printing, no multiple pages specified.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


Prints two pages per sheet.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int multiplePagesType) {#toString-int}
```
public static String toString(int multiplePagesType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
