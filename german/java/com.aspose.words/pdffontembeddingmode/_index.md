---
title: "PdfFontEmbeddingMode"
linktitle: "PdfFontEmbeddingMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Aspose.Words Schriften in Java einbetten soll."
type: docs
weight: 535
url: /de/java/com.aspose.words/pdffontembeddingmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfFontEmbeddingMode
```

Gibt an, wie Aspose.Words Schriftarten einbetten soll.

 **Examples:** 

Zeigt, wie man Aspose.Words so einstellt, dass das Einbetten der Schriften Arial und Times New Roman in ein PDF‑Dokument übersprungen wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // "Arial" is a standard font, and "Courier New" is a nonstandard font.
 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Courier New");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
 options.setEmbedFullFonts(true);

 // Set the "FontEmbeddingMode" property to "EmbedAll" to embed all fonts in the output PDF.
 // Set the "FontEmbeddingMode" property to "EmbedNonstandard" to only allow nonstandard fonts' embedding in the output PDF.
 // Set the "FontEmbeddingMode" property to "EmbedNone" to not embed any fonts in the output PDF.
 options.setFontEmbeddingMode(pdfFontEmbeddingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

 switch (pdfFontEmbeddingMode) {
     case PdfFontEmbeddingMode.EMBED_ALL:
         Assert.assertTrue(new File(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf").length() < 1047200);
         break;
     case PdfFontEmbeddingMode.EMBED_NONSTANDARD:
         Assert.assertTrue(new File(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf").length() < 491800);
         break;
     case PdfFontEmbeddingMode.EMBED_NONE:
         Assert.assertTrue(new File(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf").length() <= 4258);
         break;
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [EMBED_ALL](#EMBED-ALL) | Aspose.Words bettet alle Schriften ein. |
| [EMBED_NONE](#EMBED-NONE) | Aspose.Words bettet keine Schriften ein. |
| [EMBED_NONSTANDARD](#EMBED-NONSTANDARD) | Aspose.Words bettet alle Schriften ein, außer den standardmäßigen Windows‑Schriften Arial und Times New Roman. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfFontEmbeddingModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfFontEmbeddingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfFontEmbeddingMode)](#toString-int) |  |
### EMBED_ALL {#EMBED-ALL}
```
public static int EMBED_ALL
```


Aspose.Words bettet alle Schriften ein.

### EMBED_NONE {#EMBED-NONE}
```
public static int EMBED_NONE
```


Aspose.Words bettet keine Schriften ein.

### EMBED_NONSTANDARD {#EMBED-NONSTANDARD}
```
public static int EMBED_NONSTANDARD
```


Aspose.Words bettet alle Schriften ein, außer den standardmäßigen Windows‑Schriften Arial und Times New Roman. Nur die Schriften Arial und Times New Roman sind in diesem Modus betroffen, weil MS Word beim Speichern eines Dokuments als PDF nicht ausschließlich diese Schriften einbettet.

### length {#length}
```
public static int length
```


### fromName(String pdfFontEmbeddingModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfFontEmbeddingModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfFontEmbeddingModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfFontEmbeddingMode) {#getName-int}
```
public static String getName(int pdfFontEmbeddingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfFontEmbeddingMode) {#toString-int}
```
public static String toString(int pdfFontEmbeddingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

**Returns:**
java.lang.String
