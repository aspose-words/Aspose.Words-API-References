---
title: "TxtExportHeadersFootersMode"
linktitle: "TxtExportHeadersFootersMode"
second_title: "Aspose.Words Java için"
description: "Java'da üstbilgi ve altbilgilerin düz metin formatına nasıl dışa aktarılacağını belirtir."
type: docs
weight: 690
url: /tr/java/com.aspose.words/txtexportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtExportHeadersFootersMode
```

Üstbilgi ve altbilgilerin düz metin formatına nasıl dışa aktarılacağını belirtir.

 **Examples:** 

Üstbilgi ve altbilgilerin düz metin formatına nasıl dışa aktarılacağını belirtmeyi gösterir.

```

 Document doc = new Document();

 // Insert even and primary headers/footers into the document.
 // The primary header/footers will override the even headers/footers.
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.HEADER_EVEN));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_EVEN).appendParagraph("Even header");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.FOOTER_EVEN));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_EVEN).appendParagraph("Even footer");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.HEADER_PRIMARY));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).appendParagraph("Primary header");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.FOOTER_PRIMARY));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY).appendParagraph("Primary footer");

 // Insert pages to display these headers and footers.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Page 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Page 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions saveOptions = new TxtSaveOptions();

 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.None"
 // to not export any headers/footers.
 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.PrimaryOnly"
 // to only export primary headers/footers.
 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.AllAtEnd"
 // to place all headers and footers for all section bodies at the end of the document.
 saveOptions.setExportHeadersFootersMode(txtExportHeadersFootersMode);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

 String docText = new Document(getArtifactsDir() + "TxtSaveOptions.ExportHeadersFooters.txt").getText().trim();

 switch (txtExportHeadersFootersMode) {
     case TxtExportHeadersFootersMode.ALL_AT_END:
         Assert.assertEquals("Page 1\r" +
                 "Page 2\r" +
                 "Page 3\r" +
                 "Even header\r\r" +
                 "Primary header\r\r" +
                 "Even footer\r\r" +
                 "Primary footer", docText);

         break;
     case TxtExportHeadersFootersMode.PRIMARY_ONLY:
         Assert.assertEquals("Primary header\r" +
                 "Page 1\r" +
                 "Page 2\r" +
                 "Page 3\r" +
                 "Primary footer", docText);
         break;
     case TxtExportHeadersFootersMode.NONE:
         Assert.assertEquals("Page 1\r" +
                 "Page 2\r" +
                 "Page 3", docText);
         break;
 }
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALL_AT_END](#ALL-AT-END) | Tüm üstbilgi ve altbilgiler, belge sonunda tüm bölüm gövdelerinin ardından yer alır. |
| [NONE](#NONE) | Üstbilgi ve altbilgi dışa aktarılmaz. |
| [PRIMARY_ONLY](#PRIMARY-ONLY) | Yalnızca birincil üstbilgi ve altbilgiler, her bölümün başında ve sonunda dışa aktarılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String txtExportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getName(int txtExportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtExportHeadersFootersMode)](#toString-int) |  |
### ALL_AT_END {#ALL-AT-END}
```
public static int ALL_AT_END
```


Tüm üstbilgi ve altbilgiler, belge sonunda tüm bölüm gövdelerinin ardından yer alır.

 **Remarks:** 

Bu mod, Word'e benzer.

### NONE {#NONE}
```
public static int NONE
```


Üstbilgi ve altbilgi dışa aktarılmaz.

### PRIMARY_ONLY {#PRIMARY-ONLY}
```
public static int PRIMARY_ONLY
```


Yalnızca birincil üstbilgi ve altbilgiler, her bölümün başında ve sonunda dışa aktarılır.

 **Remarks:** 

Üstbilgi ve altbilgileri düz metne anlamlı bir şekilde çıkarmak zordur çünkü sayfalama yapılmaz.

Bu mod kullanıldığında, yalnızca birincil üstbilgi ve altbilgiler, her bölümün başında ve sonunda dışa aktarılır.

### length {#length}
```
public static int length
```


### fromName(String txtExportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtExportHeadersFootersModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtExportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtExportHeadersFootersMode) {#getName-int}
```
public static String getName(int txtExportHeadersFootersMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtExportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtExportHeadersFootersMode) {#toString-int}
```
public static String toString(int txtExportHeadersFootersMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| txtExportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
