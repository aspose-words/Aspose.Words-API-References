---
title: "HeaderFooterType"
linktitle: "HeaderFooterType"
second_title: "Aspose.Words Java için"
description: "Java'da bir Word dosyasında bulunan başlık veya altbilgi türünü tanımlar."
type: docs
weight: 372
url: /tr/java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

Bir Word dosyasında bulunan başlık veya altbilgi türünü tanımlar. Bu, bölüm başına bir başlık/altbilgi anlamına gelir. Enum değerinin plcfhdd içinde indeks olarak kullanıldığı için yeniden numaralandırmayın.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | Çift numaralı sayfalar için altbilgi. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Bölümün ilk sayfası için altbilgi. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Birincil altbilgi, ayrıca tek numaralı sayfalar için de kullanılır. |
| [HEADER_EVEN](#HEADER-EVEN) | Çift numaralı sayfalar için başlık. |
| [HEADER_FIRST](#HEADER-FIRST) | Bölümün ilk sayfası için başlık. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | Birincil başlık, ayrıca tek numaralı sayfalar için de kullanılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Çift numaralı sayfalar için altbilgi.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Bölümün ilk sayfası için altbilgi.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Birincil altbilgi, ayrıca tek numaralı sayfalar için de kullanılır.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


Çift numaralı sayfalar için başlık.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


Bölümün ilk sayfası için başlık.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


Birincil başlık, ayrıca tek numaralı sayfalar için de kullanılır.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterType) {#toString-int}
```
public static String toString(int headerFooterType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
