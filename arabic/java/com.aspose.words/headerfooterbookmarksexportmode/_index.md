---
title: "HeaderFooterBookmarksExportMode"
linktitle: "HeaderFooterBookmarksExportMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تصدير العلامات المرجعية في رؤوس/تذييلات الصفحات في Java."
type: docs
weight: 370
url: /ar/java/com.aspose.words/headerfooterbookmarksexportmode/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterBookmarksExportMode
```

يحدد كيفية تصدير العلامات المرجعية في الرؤوس/التذييلات.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ALL](#ALL) | يتم تصدير العلامات المرجعية في جميع رؤوس/تذييلات الصفحات. |
| [FIRST](#FIRST) | يتم تصدير العلامة المرجعية الوحيدة في أول رأس/تذييل للقسم. |
| [NONE](#NONE) | لا يتم تصدير العلامات المرجعية في رؤوس/تذييلات الصفحات. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String headerFooterBookmarksExportModeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterBookmarksExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterBookmarksExportMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


يتم تصدير العلامات المرجعية في جميع رؤوس/تذييلات الصفحات.

### FIRST {#FIRST}
```
public static int FIRST
```


يتم تصدير العلامة المرجعية الوحيدة في أول رأس/تذييل للقسم.

### NONE {#NONE}
```
public static int NONE
```


لا يتم تصدير العلامات المرجعية في رؤوس/تذييلات الصفحات.

### length {#length}
```
public static int length
```


### fromName(String headerFooterBookmarksExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterBookmarksExportModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| headerFooterBookmarksExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterBookmarksExportMode) {#getName-int}
```
public static String getName(int headerFooterBookmarksExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterBookmarksExportMode) {#toString-int}
```
public static String toString(int headerFooterBookmarksExportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
