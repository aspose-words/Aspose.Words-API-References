---
title: "PdfFontEmbeddingMode"
linktitle: "PdfFontEmbeddingMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo Aspose.Words debe incrustar fuentes en Java."
type: docs
weight: 535
url: /es/java/com.aspose.words/pdffontembeddingmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfFontEmbeddingMode
```

Especifica cómo Aspose.Words debe incrustar fuentes.

 **Examples:** 

Muestra cómo configurar Aspose.Words para omitir la incrustación de las fuentes Arial y Times New Roman en un documento PDF.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [EMBED_ALL](#EMBED-ALL) | Aspose.Words incrusta todas las fuentes. |
| [EMBED_NONE](#EMBED-NONE) | Aspose.Words no incrusta ninguna fuente. |
| [EMBED_NONSTANDARD](#EMBED-NONSTANDARD) | Aspose.Words incrusta todas las fuentes excepto las fuentes estándar de Windows Arial y Times New Roman. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfFontEmbeddingModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfFontEmbeddingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfFontEmbeddingMode)](#toString-int) |  |
### EMBED_ALL {#EMBED-ALL}
```
public static int EMBED_ALL
```


Aspose.Words incrusta todas las fuentes.

### EMBED_NONE {#EMBED-NONE}
```
public static int EMBED_NONE
```


Aspose.Words no incrusta ninguna fuente.

### EMBED_NONSTANDARD {#EMBED-NONSTANDARD}
```
public static int EMBED_NONSTANDARD
```


Aspose.Words incrusta todas las fuentes excepto las fuentes estándar de Windows Arial y Times New Roman. Sólo las fuentes Arial y Times New Roman se ven afectadas en este modo porque MS Word no incrusta únicamente esas fuentes al guardar el documento en PDF.

### length {#length}
```
public static int length
```


### fromName(String pdfFontEmbeddingModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfFontEmbeddingModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfFontEmbeddingModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfFontEmbeddingMode) {#getName-int}
```
public static String getName(int pdfFontEmbeddingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

**Returns:**
java.lang.String
