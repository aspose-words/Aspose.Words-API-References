---
title: "HeaderFooterType"
linktitle: "HeaderFooterType"
second_title: "Aspose.Words para Java"
description: "Identifica el tipo de encabezado o pie de página encontrado en un archivo Word en Java."
type: docs
weight: 372
url: /es/java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

Identifica el tipo de encabezado o pie de página encontrado en un archivo Word. Este es un encabezado/pie de página por sección. No renumerar ya que el valor del enum se usa como índice en plcfhdd.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | Pie de página para páginas pares. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Pie de página para la primera página de la sección. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Pie de página principal, también usado para páginas impares. |
| [HEADER_EVEN](#HEADER-EVEN) | Encabezado para páginas pares. |
| [HEADER_FIRST](#HEADER-FIRST) | Encabezado para la primera página de la sección. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | Encabezado principal, también usado para páginas impares. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Pie de página para páginas pares.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Pie de página para la primera página de la sección.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Pie de página principal, también usado para páginas impares.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


Encabezado para páginas pares.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


Encabezado para la primera página de la sección.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


Encabezado principal, también usado para páginas impares.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
