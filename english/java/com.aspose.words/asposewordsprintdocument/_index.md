---
title: AsposeWordsPrintDocument
second_title: Aspose.Words for Java API Reference
description: Provides a default implementation for printing of a  within the Java printing framework.
type: docs
weight: 14
url: /java/com.aspose.words/asposewordsprintdocument/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

Provides a default implementation for printing of a [Document](../../com.aspose.words/document) within the Java printing framework.

To learn more, visit the **Printing a Document Programmatically or Using Dialogs** documentation article.

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument) overrides both  and .

A single Aspose.Words document can consist of multiple sections that specify pages with different sizes, orientation and paper trays. [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument) should be used as  to properly print each of the different paper size, orientation, etc.

On the other hand, if the document consists of a single section only, the developer can use [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument) as  to improve printing performance.
## Constructors

| Constructor | Description |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int-) |  |
| [getNumberOfPages()](#getNumberOfPages--) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int-) |  |
| [getPrintable(int pageIndex)](#getPrintable-int-) |  |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document-}
```
public AsposeWordsPrintDocument(Document document)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | The document to print. |

### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int-}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| graphics | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**Returns:**
int
### getNumberOfPages() {#getNumberOfPages--}
```
public int getNumberOfPages()
```




**Returns:**
int
### getPageFormat(int pageIndex) {#getPageFormat-int-}
```
public PageFormat getPageFormat(int pageIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.PageFormat
### getPrintable(int pageIndex) {#getPrintable-int-}
```
public Printable getPrintable(int pageIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.Printable
