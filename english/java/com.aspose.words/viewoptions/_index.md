---
title: ViewOptions
linktitle: ViewOptions
second_title: Aspose.Words for Java
description: Provides various options that control how a document is shown in Microsoft Word in Java.
type: docs
weight: 621
url: /java/com.aspose.words/viewoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

Provides various options that control how a document is shown in Microsoft Word.

To learn more, visit the [ Work with Options and Appearance of Word Documents ][Work with Options and Appearance of Word Documents] documentation article.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```


[Work with Options and Appearance of Word Documents]: https://docs.aspose.com/words/java/work-with-word-document-options-and-appearance/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape) | Controls display of the background shape in print layout view. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries) | Turns off display of the space between the top of the text and the top edge of the page. |
| [getFormsDesign()](#getFormsDesign) | Specifies whether the document is in forms design mode. |
| [getViewType()](#getViewType) | Controls the view mode in Microsoft Word. |
| [getZoomPercent()](#getZoomPercent) | Gets the percentage (between 10 and 500) at which you want to view your document. |
| [getZoomType()](#getZoomType) | Gets a zoom value based on the size of the window. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean) | Controls display of the background shape in print layout view. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean) | Turns off display of the space between the top of the text and the top edge of the page. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean) | Specifies whether the document is in forms design mode. |
| [setViewType(int value)](#setViewType-int) | Controls the view mode in Microsoft Word. |
| [setZoomPercent(int value)](#setZoomPercent-int) | Sets the percentage (between 10 and 500) at which you want to view your document. |
| [setZoomType(int value)](#setZoomType-int) | Sets a zoom value based on the size of the window. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getDisplayBackgroundShape() {#getDisplayBackgroundShape}
```
public boolean getDisplayBackgroundShape()
```


Controls display of the background shape in print layout view.

 **Examples:** 

Shows how to hide/display document background images in view options.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries}
```
public boolean getDoNotDisplayPageBoundaries()
```


Turns off display of the space between the top of the text and the top edge of the page.

 **Examples:** 

Shows how to hide vertical whitespace and headers/footers in view options.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getFormsDesign() {#getFormsDesign}
```
public boolean getFormsDesign()
```


Specifies whether the document is in forms design mode.

 **Remarks:** 

Currently works only for documents in WordML format.

 **Examples:** 

Shows how to enable/disable forms design mode.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getViewType() {#getViewType}
```
public int getViewType()
```


Controls the view mode in Microsoft Word.

 **Remarks:** 

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [ViewType](../../com.aspose.words/viewtype/) constants.
### getZoomPercent() {#getZoomPercent}
```
public int getZoomPercent()
```


Gets the percentage (between 10 and 500) at which you want to view your document.

 **Remarks:** 

If value is 0 then this property uses 100 instead, else if value is less than 10 or greater than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Returns:**
int - The percentage (between 10 and 500) at which you want to view your document.
### getZoomType() {#getZoomType}
```
public int getZoomType()
```


Gets a zoom value based on the size of the window.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Returns:**
int - A zoom value based on the size of the window. The returned value is one of [ZoomType](../../com.aspose.words/zoomtype/) constants.
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




### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean}
```
public void setDisplayBackgroundShape(boolean value)
```


Controls display of the background shape in print layout view.

 **Examples:** 

Shows how to hide/display document background images in view options.

```

 // Use an HTML string to create a new document with a flat background color.
 final String HTML =
         "\r\n                \r\n                    Hello world!\r\n                \r\n            ";

 Document doc = new Document(new ByteArrayInputStream(HTML.getBytes()));

 // The source for the document has a flat color background,
 // the presence of which will set the "DisplayBackgroundShape" flag to "true".
 Assert.assertTrue(doc.getViewOptions().getDisplayBackgroundShape());

 // Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
 // This may affect some text colors to improve visibility.
 // Set the "DisplayBackgroundShape" to "false" to not display the background color.
 doc.getViewOptions().setDisplayBackgroundShape(displayBackgroundShape);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayBackgroundShape.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Turns off display of the space between the top of the text and the top edge of the page.

 **Examples:** 

Shows how to hide vertical whitespace and headers/footers in view options.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert content that spans across 3 pages.
 builder.writeln("Paragraph 1, Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 2, Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Paragraph 3, Page 3.");

 // Insert a header and a footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("This is the footer.");

 // This document contains a small amount of content that takes up a few full pages worth of space.
 // Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
 // footers, and much of the vertical whitespace when displaying our document.
 // Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
 // to normally display our document.
 doc.getViewOptions().setDoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

 doc.save(getArtifactsDir() + "ViewOptions.DisplayPageBoundaries.doc");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean}
```
public void setFormsDesign(boolean value)
```


Specifies whether the document is in forms design mode.

 **Remarks:** 

Currently works only for documents in WordML format.

 **Examples:** 

Shows how to enable/disable forms design mode.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "FormsDesign" property to "false" to keep forms design mode disabled.
 // Set the "FormsDesign" property to "true" to enable forms design mode.
 doc.getViewOptions().setFormsDesign(useFormsDesign);

 doc.save(getArtifactsDir() + "ViewOptions.FormsDesign.xml");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setViewType(int value) {#setViewType-int}
```
public void setViewType(int value)
```


Controls the view mode in Microsoft Word.

 **Remarks:** 

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ViewType](../../com.aspose.words/viewtype/) constants. |

### setZoomPercent(int value) {#setZoomPercent-int}
```
public void setZoomPercent(int value)
```


Sets the percentage (between 10 and 500) at which you want to view your document.

 **Remarks:** 

If value is 0 then this property uses 100 instead, else if value is less than 10 or greater than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The percentage (between 10 and 500) at which you want to view your document. |

### setZoomType(int value) {#setZoomType-int}
```
public void setZoomType(int value)
```


Sets a zoom value based on the size of the window.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A zoom value based on the size of the window. The value must be one of [ZoomType](../../com.aspose.words/zoomtype/) constants. |

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

