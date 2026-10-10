---
title: "PdfPageMode"
linktitle: "PdfPageMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF في Java."
type: docs
weight: 540
url: /ar/java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF.

 **Examples:** 

يوضح كيفية معالجة العلامات المرجعية في رؤوس/تذييلات الصفحات في مستند نقوم بتحويله إلى PDF.

```

 Document doc = new Document(getMyDir() + "Bookmarks in headers and footers.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
 saveOptions.setPageMode(PdfPageMode.USE_OUTLINES);

 // Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
 // bookmarks at the first level of the outline in the output PDF.
 saveOptions.getOutlineOptions().setDefaultBookmarksOutlineLevel(1);

 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
 // not export any bookmarks that are inside headers/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
 // only export bookmarks in the first section's header/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
 // export bookmarks that are in all headers/footers.
 saveOptions.setHeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
 
```

يُظهر كيفية ضبط التعليمات لبعض قارئات PDF لتتبعها عند فتح مستند الإخراج.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.FullScreen" to get the PDF reader to open the saved
 // document in full-screen mode, which takes over the monitor's display and has no controls visible.
 // Set the "PageMode" property to "PdfPageMode.UseThumbs" to get the PDF reader to display a separate panel
 // with a thumbnail for each page in the document.
 // Set the "PageMode" property to "PdfPageMode.UseOC" to get the PDF reader to display a separate panel
 // that allows us to work with any layers present in the document.
 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to get the PDF reader
 // also to display the outline, if possible.
 // Set the "PageMode" property to "PdfPageMode.UseNone" to get the PDF reader to display just the document itself.
 // Set the "PageMode" property to "PdfPageMode.UseAttachments" to make visible attachments panel.
 options.setPageMode(pageMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageMode.pdf", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | وضع ملء الشاشة، دون شريط قوائم أو أدوات تحكم النافذة أو أي نافذة أخرى مرئية. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | لوحة المرفقات مرئية. |
| [USE_NONE](#USE-NONE) | لا مخطط المستند ولا صور المصغرات مرئية. |
| [USE_OC](#USE-OC) | لوحة مجموعة المحتوى الاختيارية مرئية. |
| [USE_OUTLINES](#USE-OUTLINES) | مخطط المستند مرئي. |
| [USE_THUMBS](#USE-THUMBS) | صور المصغرات مرئية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


وضع ملء الشاشة، دون شريط قوائم أو أدوات تحكم النافذة أو أي نافذة أخرى مرئية.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


لوحة المرفقات مرئية.

 **Remarks:** 

غير مدعوم في إصدارات PDF التالية: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


لا مخطط المستند ولا صور المصغرات مرئية.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


لوحة مجموعة المحتوى الاختيارية مرئية.

 **Remarks:** 

غير مدعوم في إصدارات PDF التالية: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


مخطط المستند مرئي. لاحظ أنه إذا لم يكن هناك مخططات في مستند PDF فإن لوحة تنقل المخطط لن تكون مرئية على أي حال.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


صور المصغرات مرئية.

### length {#length}
```
public static int length
```


### fromName(String pdfPageModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageMode) {#getName-int}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPageMode) {#toString-int}
```
public static String toString(int pdfPageMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
