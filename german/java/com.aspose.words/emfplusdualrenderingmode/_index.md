---
title: "EmfPlusDualRenderingMode"
linktitle: "EmfPlusDualRenderingMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Aspose.Words EMF‑Dual‑Metadateien in Java rendern soll."
type: docs
weight: 186
url: /de/java/com.aspose.words/emfplusdualrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class EmfPlusDualRenderingMode
```

Gibt an, wie Aspose.Words EMF+ Dual-Metadateien rendern soll.

 **Examples:** 

Zeigt, wie man renderbezogene Optionen für Enhanced Windows Metafile beim Speichern als PDF konfiguriert.

```

 Document doc = new Document(getMyDir() + "EMF.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.Emf"
 // to only render the EMF part of an EMF+ dual metafile.
 // Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlus" to
 // to render the EMF+ part of an EMF+ dual metafile.
 // Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlusWithFallback"
 // to render the EMF+ part of an EMF+ dual metafile if all of the EMF+ records are supported.
 // Otherwise, Aspose.Words will render the EMF part.
 saveOptions.getMetafileRenderingOptions().setEmfPlusDualRenderingMode(renderingMode);

 // Set the "UseEmfEmbeddedToWmf" property to "true" to render embedded EMF data
 // for metafiles that we can render as vector graphics.
 saveOptions.getMetafileRenderingOptions().setUseEmfEmbeddedToWmf(true);

 doc.save(getArtifactsDir() + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [EMF](#EMF) | Aspose.Words rendert den EMF‑Teil der EMF+‑Dual‑Metadatei. |
| [EMF_PLUS](#EMF-PLUS) | Aspose.Words rendert den EMF+‑Teil der EMF+‑Dual‑Metadatei. |
| [EMF_PLUS_WITH_FALLBACK](#EMF-PLUS-WITH-FALLBACK) | Aspose.Words versucht, den EMF+-Teil der EMF+ Dual-Metadatei darzustellen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String emfPlusDualRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int emfPlusDualRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emfPlusDualRenderingMode)](#toString-int) |  |
### EMF {#EMF}
```
public static int EMF
```


Aspose.Words rendert den EMF‑Teil der EMF+‑Dual‑Metadatei.

### EMF_PLUS {#EMF-PLUS}
```
public static int EMF_PLUS
```


Aspose.Words rendert den EMF+‑Teil der EMF+‑Dual‑Metadatei.

### EMF_PLUS_WITH_FALLBACK {#EMF-PLUS-WITH-FALLBACK}
```
public static int EMF_PLUS_WITH_FALLBACK
```


Aspose.Words versucht, den EMF+-Teil der EMF+ Dual-Metadatei darzustellen. Wenn einige der EMF+-Datensätze nicht unterstützt werden, rendert Aspose.Words den EMF-Teil der EMF+ Dual-Metadatei.

### length {#length}
```
public static int length
```


### fromName(String emfPlusDualRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String emfPlusDualRenderingModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| emfPlusDualRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int emfPlusDualRenderingMode) {#getName-int}
```
public static String getName(int emfPlusDualRenderingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| emfPlusDualRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emfPlusDualRenderingMode) {#toString-int}
```
public static String toString(int emfPlusDualRenderingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| emfPlusDualRenderingMode | int |  |

**Returns:**
java.lang.String
