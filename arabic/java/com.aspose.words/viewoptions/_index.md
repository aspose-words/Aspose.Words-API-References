---
title: "ViewOptions"
linktitle: "ViewOptions"
second_title: "Aspose.Words لـ Java"
description: "يوفر خيارات متعددة تتحكم في كيفية عرض المستند في Microsoft Word باستخدام Java."
type: docs
weight: 714
url: /ar/java/com.aspose.words/viewoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

يوفر خيارات متعددة تتحكم في كيفية عرض المستند في Microsoft Word.

لمزيد من المعلومات، قم بزيارة مقالة الوثائق [ Work with Options and Appearance of Word Documents ][Work with Options and Appearance of Word Documents].

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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

يظهر كيفية تعيين نوع تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape) | يتحكم في عرض الشكل الخلفي في عرض تخطيط الطباعة. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries) | يقوم بإيقاف عرض المسافة بين أعلى النص وحافة الصفحة العليا. |
| [getFormsDesign()](#getFormsDesign) | يحدد ما إذا كان المستند في وضع تصميم النماذج. |
| [getViewType()](#getViewType) | يتحكم في وضع العرض في Microsoft Word. |
| [getZoomPercent()](#getZoomPercent) | يحصل على النسبة المئوية التي تريد عرض المستند بها. |
| [getZoomType()](#getZoomType) | يحصل على قيمة التكبير بناءً على حجم النافذة. |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean) | يتحكم في عرض الشكل الخلفي في عرض تخطيط الطباعة. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean) | يقوم بإيقاف عرض المسافة بين أعلى النص وحافة الصفحة العليا. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean) | يحدد ما إذا كان المستند في وضع تصميم النماذج. |
| [setViewType(int value)](#setViewType-int) | يتحكم في وضع العرض في Microsoft Word. |
| [setZoomPercent(int value)](#setZoomPercent-int) | يضبط النسبة المئوية التي تريد عرض المستند بها. |
| [setZoomType(int value)](#setZoomType-int) | يضبط قيمة التكبير بناءً على حجم النافذة. |
### getDisplayBackgroundShape() {#getDisplayBackgroundShape}
```
public boolean getDisplayBackgroundShape()
```


يتحكم في عرض الشكل الخلفي في عرض تخطيط الطباعة.

 **Examples:** 

يظهر كيفية إخفاء/عرض صور خلفية المستند في خيارات العرض.

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
boolean - القيمة المنطقية المقابلة.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries}
```
public boolean getDoNotDisplayPageBoundaries()
```


يقوم بإيقاف عرض المسافة بين أعلى النص وحافة الصفحة العليا.

 **Examples:** 

يظهر كيفية إخفاء المسافات الرأسية والرؤوس/التذييلات في خيارات العرض.

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
boolean - القيمة المنطقية المقابلة.
### getFormsDesign() {#getFormsDesign}
```
public boolean getFormsDesign()
```


يحدد ما إذا كان المستند في وضع تصميم النماذج.

 **Remarks:** 

يعمل حاليًا فقط مع المستندات بتنسيق WordML.

 **Examples:** 

يظهر كيفية تمكين/تعطيل وضع تصميم النماذج.

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
boolean - القيمة المنطقية المقابلة.
### getViewType() {#getViewType}
```
public int getViewType()
```


يتحكم في وضع العرض في Microsoft Word.

 **Remarks:** 

على الرغم من أن Aspose.Words قادر على قراءة وكتابة هذا الخيار، فإن استخدامه يخص التطبيق. على سبيل المثال لا يحترم MS Word 2013 قيمة هذا الخيار.

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [ViewType](../../com.aspose.words/viewtype/).
### getZoomPercent() {#getZoomPercent}
```
public int getZoomPercent()
```


يحصل على النسبة المئوية التي تريد عرض المستند بها.

 **Remarks:** 

على الرغم من أن Aspose.Words قادر على قراءة وكتابة هذا الخيار، فإن استخدامه يخص التطبيق. على سبيل المثال لا يحترم MS Word 2013 قيمة هذا الخيار.

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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
int - النسبة المئوية التي تريد عرض المستند بها.
### getZoomType() {#getZoomType}
```
public int getZoomType()
```


يحصل على قيمة التكبير بناءً على حجم النافذة.

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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

يظهر كيفية تعيين نوع تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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
int - قيمة تكبير بناءً على حجم النافذة. القيمة المرجعة هي واحدة من ثوابت [ZoomType](../../com.aspose.words/zoomtype/).
### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean}
```
public void setDisplayBackgroundShape(boolean value)
```


يتحكم في عرض الشكل الخلفي في عرض تخطيط الطباعة.

 **Examples:** 

يظهر كيفية إخفاء/عرض صور خلفية المستند في خيارات العرض.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


يقوم بإيقاف عرض المسافة بين أعلى النص وحافة الصفحة العليا.

 **Examples:** 

يظهر كيفية إخفاء المسافات الرأسية والرؤوس/التذييلات في خيارات العرض.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean}
```
public void setFormsDesign(boolean value)
```


يحدد ما إذا كان المستند في وضع تصميم النماذج.

 **Remarks:** 

يعمل حاليًا فقط مع المستندات بتنسيق WordML.

 **Examples:** 

يظهر كيفية تمكين/تعطيل وضع تصميم النماذج.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setViewType(int value) {#setViewType-int}
```
public void setViewType(int value)
```


يتحكم في وضع العرض في Microsoft Word.

 **Remarks:** 

على الرغم من أن Aspose.Words قادر على قراءة وكتابة هذا الخيار، فإن استخدامه يخص التطبيق. على سبيل المثال لا يحترم MS Word 2013 قيمة هذا الخيار.

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [ViewType](../../com.aspose.words/viewtype/). |

### setZoomPercent(int value) {#setZoomPercent-int}
```
public void setZoomPercent(int value)
```


يضبط النسبة المئوية التي تريد عرض المستند بها.

 **Remarks:** 

على الرغم من أن Aspose.Words قادر على قراءة وكتابة هذا الخيار، فإن استخدامه يخص التطبيق. على سبيل المثال لا يحترم MS Word 2013 قيمة هذا الخيار.

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | النسبة المئوية التي تريد عرض المستند بها. |

### setZoomType(int value) {#setZoomType-int}
```
public void setZoomType(int value)
```


يضبط قيمة التكبير بناءً على حجم النافذة.

 **Examples:** 

يظهر كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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

يظهر كيفية تعيين نوع تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | قيمة تكبير بناءً على حجم النافذة. يجب أن تكون القيمة واحدة من ثوابت [ZoomType](../../com.aspose.words/zoomtype/). |

