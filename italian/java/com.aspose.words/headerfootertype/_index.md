---
title: "HeaderFooterType"
linktitle: "HeaderFooterType"
second_title: "Aspose.Words per Java"
description: "Identifica il tipo di intestazione o piè di pagina presente in un file Word in Java."
type: docs
weight: 372
url: /it/java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

Identifica il tipo di intestazione o piè di pagina presente in un file Word.  Questo è un'intestazione/piè di pagina per sezione. Non rinumerare poiché il valore dell'enum è usato come indice in plcfhdd.

 **Examples:** 

Mostra come creare intestazioni e piè di pagina in un documento usando DocumentBuilder.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | Piè di pagina per pagine pari. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Piè di pagina per la prima pagina della sezione. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Piè di pagina principale, usato anche per pagine dispari. |
| [HEADER_EVEN](#HEADER-EVEN) | Intestazione per pagine pari. |
| [HEADER_FIRST](#HEADER-FIRST) | Intestazione per la prima pagina della sezione. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | Intestazione principale, usata anche per pagine dispari. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Piè di pagina per pagine pari.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Piè di pagina per la prima pagina della sezione.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Piè di pagina principale, usato anche per pagine dispari.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


Intestazione per pagine pari.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


Intestazione per la prima pagina della sezione.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


Intestazione principale, usata anche per pagine dispari.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
