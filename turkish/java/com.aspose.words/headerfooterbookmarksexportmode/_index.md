---
title: "HeaderFooterBookmarksExportMode"
linktitle: "HeaderFooterBookmarksExportMode"
second_title: "Aspose.Words Java için"
description: "Java'da üstbilgi/altbilgi yer imlerinin nasıl dışa aktarıldığını belirtir."
type: docs
weight: 370
url: /tr/java/com.aspose.words/headerfooterbookmarksexportmode/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterBookmarksExportMode
```

Başlık/altbilgi içindeki yer imlerinin nasıl dışa aktarıldığını belirtir.

 **Examples:** 

PDF'ye render ettiğimiz bir belgede üstbilgi/altbilgi yer imlerini nasıl işleyeceğimizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALL](#ALL) | Tüm üstbilgi/altbilgi yer imleri dışa aktarılır. |
| [FIRST](#FIRST) | Sadece bölümün ilk üstbilgi/altbilgi yer imi dışa aktarılır. |
| [NONE](#NONE) | Üstbilgi/altbilgi yer imleri dışa aktarılmaz. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String headerFooterBookmarksExportModeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterBookmarksExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterBookmarksExportMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Tüm üstbilgi/altbilgi yer imleri dışa aktarılır.

### FIRST {#FIRST}
```
public static int FIRST
```


Sadece bölümün ilk üstbilgi/altbilgi yer imi dışa aktarılır.

### NONE {#NONE}
```
public static int NONE
```


Üstbilgi/altbilgi yer imleri dışa aktarılmaz.

### length {#length}
```
public static int length
```


### fromName(String headerFooterBookmarksExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterBookmarksExportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterBookmarksExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterBookmarksExportMode) {#getName-int}
```
public static String getName(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
