---
title: "TxtExportHeadersFootersMode"
linktitle: "TxtExportHeadersFootersMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Kopf- und Fußzeilen im Klartextformat in Java exportiert werden."
type: docs
weight: 690
url: /de/java/com.aspose.words/txtexportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtExportHeadersFootersMode
```

Gibt an, wie Kopf- und Fußzeilen in das Klartextformat exportiert werden.

 **Examples:** 

Zeigt, wie man festlegt, wie Kopf- und Fußzeilen im Klartextformat exportiert werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALL_AT_END](#ALL-AT-END) | Alle Kopf- und Fußzeilen werden nach allen Abschnittsinhalten ganz am Ende eines Dokuments platziert. |
| [NONE](#NONE) | Keine Kopf- und Fußzeilen werden exportiert. |
| [PRIMARY_ONLY](#PRIMARY-ONLY) | Nur primäre Kopf- und Fußzeilen werden zu Beginn und am Ende jedes Abschnitts exportiert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String txtExportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getName(int txtExportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtExportHeadersFootersMode)](#toString-int) |  |
### ALL_AT_END {#ALL-AT-END}
```
public static int ALL_AT_END
```


Alle Kopf- und Fußzeilen werden nach allen Abschnittsinhalten ganz am Ende eines Dokuments platziert.

 **Remarks:** 

Dieser Modus ist ähnlich zu Word.

### NONE {#NONE}
```
public static int NONE
```


Keine Kopf- und Fußzeilen werden exportiert.

### PRIMARY_ONLY {#PRIMARY-ONLY}
```
public static int PRIMARY_ONLY
```


Nur primäre Kopf- und Fußzeilen werden zu Beginn und am Ende jedes Abschnitts exportiert.

 **Remarks:** 

Es ist schwierig, Kopf- und Fußzeilen sinnvoll in Klartext auszugeben, da es nicht paginiert ist.

Wenn dieser Modus verwendet wird, werden nur primäre Kopf- und Fußzeilen zu Beginn und am Ende jedes Abschnitts exportiert.

### length {#length}
```
public static int length
```


### fromName(String txtExportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtExportHeadersFootersModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| txtExportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtExportHeadersFootersMode) {#getName-int}
```
public static String getName(int txtExportHeadersFootersMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| txtExportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
