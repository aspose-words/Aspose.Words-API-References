---
title: AsposeWordsPrintDocument
linktitle: AsposeWordsPrintDocument
second_title: Aspose.Words for Java API Reference
description: Provides a default implementation for printing of a  within the Java printing framework in Java.
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

Provides a default implementation for printing of a [Document](../../com.aspose.words/document/) within the Java printing framework.

To learn more, visit the [ Printing a Document Programmatically or Using Dialogs ][Printing a Document Programmatically or Using Dialogs] documentation article.

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) overrides both  and .

A single Aspose.Words document can consist of multiple sections that specify pages with different sizes, orientation and paper trays. [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) should be used as  to properly print each of the different paper size, orientation, etc.

On the other hand, if the document consists of a single section only, the developer can use [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) as  to improve printing performance.


[Printing a Document Programmatically or Using Dialogs]: https://docs.aspose.com/words/java/print-a-document-programmatically-or-using-dialogs/
## Constructors

| Constructor | Description |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getColorMode()](#getColorMode) | Gets how non-colored pages are printed if the device supports color printing. |
| [getColorPagesPrinted()](#getColorPagesPrinted) | Gets the number of pages printed in color (i.e. |
| [getNumberOfPages()](#getNumberOfPages) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int) |  |
| [getPrintable(int pageIndex)](#getPrintable-int) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int) |  |
| [setColorMode(int value)](#setColorMode-int) | Sets how non-colored pages are printed if the device supports color printing. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document}
```
public AsposeWordsPrintDocument(Document document)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | The document to print. |

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Gets how non-colored pages are printed if the device supports color printing. Doesn't affect booklet printing.

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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




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


Sets how non-colored pages are printed if the device supports color printing. Doesn't affect booklet printing.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | How non-colored pages are printed if the device supports color printing. The value must be one of [ColorPrintMode](../../com.aspose.words/colorprintmode/) constants. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

