---
title: "HeaderFooterType"
linktitle: "HeaderFooterType"
second_title: "Aspose.Words pour Java"
description: "Identifie le type d’en-tête ou de pied de page trouvé dans un fichier Word en Java."
type: docs
weight: 372
url: /fr/java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

Identifie le type d’en-tête ou de pied de page trouvé dans un fichier Word.  Il s’agit d’un en-tête/pied de page par section. Ne pas renuméroter car la valeur de l’énumération est utilisée comme index dans plcfhdd.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

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
## Champs

| Champ | Description |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | Pied de page pour les pages paires. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Pied de page pour la première page de la section. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Pied de page principal, également utilisé pour les pages impaires. |
| [HEADER_EVEN](#HEADER-EVEN) | En-tête pour les pages paires. |
| [HEADER_FIRST](#HEADER-FIRST) | En-tête pour la première page de la section. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | En-tête principal, également utilisé pour les pages impaires. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Pied de page pour les pages paires.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Pied de page pour la première page de la section.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Pied de page principal, également utilisé pour les pages impaires.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


En-tête pour les pages paires.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


En-tête pour la première page de la section.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


En-tête principal, également utilisé pour les pages impaires.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
