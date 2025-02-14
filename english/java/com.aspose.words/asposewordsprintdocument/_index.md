---
title: AsposeWordsPrintDocument
linktitle: AsposeWordsPrintDocument
second_title: Aspose.Words for Java
description: Provides a default implementation for printing of a Document within the Java printing framework in Java.
type: docs
weight: 20
url: /java/com.aspose.words/asposewordsprintdocument/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

Provides a default implementation for printing of a [Document](../../com.aspose.words/document/) within the Java printing framework.

To learn more, visit the [ Printing a Document Programmatically or Using Dialogs ][Printing a Document Programmatically or Using Dialogs] documentation article.

 **Remarks:** 

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) overrides both **java.awt.print.Printable** and **java.awt.print.Pageable**.

A single Aspose.Words document can consist of multiple sections that specify pages with different sizes, orientation and paper trays. [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) should be used as **java.awt.print.Pageable** to properly print each of the different paper size, orientation, etc.

On the other hand, if the document consists of a single section only, the developer can use [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) as **java.awt.print.Printable** to improve printing performance.


[Printing a Document Programmatically or Using Dialogs]: https://docs.aspose.com/words/java/print-a-document-programmatically-or-using-dialogs/
## Constructors

| Constructor | Description |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getColorMode()](#getColorMode) | Gets how non-colored pages are printed if the device supports color printing. |
| [getColorPagesPrinted()](#getColorPagesPrinted) | Gets the number of pages printed in color (i.e. |
| [getNumberOfPages()](#getNumberOfPages) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int) |  |
| [getPrintable(int pageIndex)](#getPrintable-int) |  |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int) |  |
| [setColorMode(int value)](#setColorMode-int) | Sets how non-colored pages are printed if the device supports color printing. |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document}
```
public AsposeWordsPrintDocument(Document document)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | The document to print. |

### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Gets how non-colored pages are printed if the device supports color printing.

 **Remarks:** 

Doesn't affect booklet printing.

**Returns:**
int - How non-colored pages are printed if the device supports color printing. The returned value is one of [ColorPrintMode](../../com.aspose.words/colorprintmode/) constants.
### getColorPagesPrinted() {#getColorPagesPrinted}
```
public int getColorPagesPrinted()
```


Gets the number of pages printed in color (i.e. with PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) set to true).

**Returns:**
int - The number of pages printed in color (i.e.
### getNumberOfPages() {#getNumberOfPages}
```
public int getNumberOfPages()
```




**Returns:**
int
### getPageFormat(int pageIndex) {#getPageFormat-int}
```
public PageFormat getPageFormat(int pageIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.PageFormat
### getPrintable(int pageIndex) {#getPrintable-int}
```
public Printable getPrintable(int pageIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.Printable
### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int}
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
### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Sets how non-colored pages are printed if the device supports color printing.

 **Remarks:** 

Doesn't affect booklet printing.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | How non-colored pages are printed if the device supports color printing. The value must be one of [ColorPrintMode](../../com.aspose.words/colorprintmode/) constants. |

