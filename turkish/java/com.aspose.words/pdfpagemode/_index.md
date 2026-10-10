---
title: "PdfPageMode"
linktitle: "PdfPageMode"
second_title: "Aspose.Words Java için"
description: "PDF belgesinin Java'daki PDF okuyucusunda açıldığında nasıl görüntüleneceğini belirtir."
type: docs
weight: 540
url: /tr/java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

PDF belgesinin PDF okuyucusunda açıldığında nasıl görüntüleneceğini belirtir.

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

Çıktı belgesini açarken bazı PDF okuyucularının izlemesi için talimatların nasıl ayarlanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | Menü çubuğu, pencere kontrolleri veya başka bir pencere görünmeyen tam ekran modu. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | Ekler paneli görünür. |
| [USE_NONE](#USE-NONE) | Ne belge taslağı ne de küçük resim görüntüleri görünür. |
| [USE_OC](#USE-OC) | İsteğe bağlı içerik grubu paneli görünür. |
| [USE_OUTLINES](#USE-OUTLINES) | Belge taslağı görünür. |
| [USE_THUMBS](#USE-THUMBS) | Küçük resimler görünür. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Menü çubuğu, pencere kontrolleri veya başka bir pencere görünmeyen tam ekran modu.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


Ekler paneli görünür.

 **Remarks:** 

Aşağıdaki PDF sürümlerinde desteklenmez: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Ne belge taslağı ne de küçük resim görüntüleri görünür.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


İsteğe bağlı içerik grubu paneli görünür.

 **Remarks:** 

Aşağıdaki PDF sürümlerinde desteklenmez: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


Belge taslağı görünür. PDF belgesinde taslak yoksa, taslak gezinme bölmesi yine de görünmez.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


Küçük resimler görünür.

### length {#length}
```
public static int length
```


### fromName(String pdfPageModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageMode) {#getName-int}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
