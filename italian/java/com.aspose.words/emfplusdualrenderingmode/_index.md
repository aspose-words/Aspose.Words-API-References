---
title: "EmfPlusDualRenderingMode"
linktitle: "EmfPlusDualRenderingMode"
second_title: "Aspose.Words per Java"
description: "Specifica come Aspose.Words deve renderizzare i metafili EMF Dual in Java."
type: docs
weight: 186
url: /it/java/com.aspose.words/emfplusdualrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class EmfPlusDualRenderingMode
```

Specifica come Aspose.Words deve renderizzare i metafili EMF+ Dual.

 **Examples:** 

Mostra come configurare le opzioni di rendering relative a Enhanced Windows Metafile durante il salvataggio in PDF.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [EMF](#EMF) | Aspose.Words renderizza la parte EMF del metafile EMF+ Dual. |
| [EMF_PLUS](#EMF-PLUS) | Aspose.Words renderizza la parte EMF+ del metafile EMF+ Dual. |
| [EMF_PLUS_WITH_FALLBACK](#EMF-PLUS-WITH-FALLBACK) | Aspose.Words tenta di renderizzare la parte EMF+ del metafile EMF+ Dual. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String emfPlusDualRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int emfPlusDualRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emfPlusDualRenderingMode)](#toString-int) |  |
### EMF {#EMF}
```
public static int EMF
```


Aspose.Words renderizza la parte EMF del metafile EMF+ Dual.

### EMF_PLUS {#EMF-PLUS}
```
public static int EMF_PLUS
```


Aspose.Words renderizza la parte EMF+ del metafile EMF+ Dual.

### EMF_PLUS_WITH_FALLBACK {#EMF-PLUS-WITH-FALLBACK}
```
public static int EMF_PLUS_WITH_FALLBACK
```


Aspose.Words tenta di renderizzare la parte EMF+ del metafile EMF+ Dual. Se alcuni dei record EMF+ non sono supportati, Aspose.Words renderizza la parte EMF del metafile EMF+ Dual.

### length {#length}
```
public static int length
```


### fromName(String emfPlusDualRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String emfPlusDualRenderingModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| emfPlusDualRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int emfPlusDualRenderingMode) {#getName-int}
```
public static String getName(int emfPlusDualRenderingMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| emfPlusDualRenderingMode | int |  |

**Returns:**
java.lang.String
