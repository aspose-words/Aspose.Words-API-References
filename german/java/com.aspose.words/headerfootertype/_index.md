---
title: "HeaderFooterType"
linktitle: "HeaderFooterType"
second_title: "Aspose.Words für Java"
description: "Identifiziert den Typ von Kopf- oder Fußzeile, die in einer Word-Datei in Java gefunden wird."
type: docs
weight: 372
url: /de/java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

Identifiziert den Typ von Kopf- oder Fußzeile, die in einer Word-Datei gefunden wird. Dies ist eine Kopf-/Fußzeile pro Abschnitt. Nicht neu nummerieren, da der Wert des Enums als Index in plcfhdd verwendet wird.

 **Examples:** 

Zeigt, wie man Kopf- und Fußzeilen in einem Dokument mit DocumentBuilder erstellt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | Fußzeile für gerade Seiten. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Fußzeile für die erste Seite des Abschnitts. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Primäre Fußzeile, die auch für ungerade Seiten verwendet wird. |
| [HEADER_EVEN](#HEADER-EVEN) | Kopfzeile für gerade Seiten. |
| [HEADER_FIRST](#HEADER-FIRST) | Kopfzeile für die erste Seite des Abschnitts. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | Primäre Kopfzeile, die auch für ungerade Seiten verwendet wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Fußzeile für gerade Seiten.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Fußzeile für die erste Seite des Abschnitts.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Primäre Fußzeile, die auch für ungerade Seiten verwendet wird.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


Kopfzeile für gerade Seiten.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


Kopfzeile für die erste Seite des Abschnitts.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


Primäre Kopfzeile, die auch für ungerade Seiten verwendet wird.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
