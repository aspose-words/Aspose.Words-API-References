---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words لـ Java"
description: "يحدد تخطيط الصفحة الذي سيُستخدم عند فتح المستند في قارئ PDF باستخدام Java."
type: docs
weight: 539
url: /ar/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

يحدد تخطيط الصفحة الذي سيُستخدم عند فتح المستند في قارئ PDF.

 **Examples:** 

يظهر كيفية عرض الصفحات عند فتحها في قارئ PDF.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | عرض الصفحات في عمود واحد. |
| [SINGLE_PAGE](#SINGLE-PAGE) | عرض صفحة واحدة في كل مرة. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | عرض الصفحات في عمودين، مع الصفحات ذات الأرقام الفردية على اليسار. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | عرض الصفحات في عمودين، مع الصفحات ذات الأرقام الفردية على اليمين. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | عرض الصفحات صفحتين في كل مرة، مع الصفحات ذات الأرقام الفردية على اليسار. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | عرض الصفحات صفحتين في كل مرة، مع الصفحات ذات الأرقام الفردية على اليمين. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


عرض الصفحات في عمود واحد.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


عرض صفحة واحدة في كل مرة.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


عرض الصفحات في عمودين، مع الصفحات ذات الأرقام الفردية على اليسار.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


عرض الصفحات في عمودين، مع الصفحات ذات الأرقام الفردية على اليمين.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


عرض الصفحات صفحتين في كل مرة، مع الصفحات ذات الأرقام الفردية على اليسار.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


عرض الصفحات صفحتين في كل مرة، مع الصفحات ذات الأرقام الفردية على اليمين.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPageLayout) {#toString-int}
```
public static String toString(int pdfPageLayout)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
