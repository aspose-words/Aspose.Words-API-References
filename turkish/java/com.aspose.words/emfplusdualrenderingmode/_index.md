---
title: "EmfPlusDualRenderingMode"
linktitle: "EmfPlusDualRenderingMode"
second_title: "Aspose.Words Java için"
description: "Java'da Aspose.Words'un EMF Dual metafilelerini nasıl işleyeceğini belirtir."
type: docs
weight: 186
url: /tr/java/com.aspose.words/emfplusdualrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class EmfPlusDualRenderingMode
```

Aspose.Words'ün EMF+ Dual meta dosyalarını nasıl oluşturması gerektiğini belirtir.

 **Examples:** 

PDF'ye kaydederken Gelişmiş Windows Metafile ile ilgili işleme seçeneklerini nasıl yapılandıracağınızı gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [EMF](#EMF) | Aspose.Words, EMF+ Dual metafilenin EMF kısmını işler. |
| [EMF_PLUS](#EMF-PLUS) | Aspose.Words, EMF+ Dual metafilenin EMF+ kısmını işler. |
| [EMF_PLUS_WITH_FALLBACK](#EMF-PLUS-WITH-FALLBACK) | Aspose.Words, EMF+ Dual metafilenin EMF+ kısmını işlemeye çalışır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String emfPlusDualRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int emfPlusDualRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emfPlusDualRenderingMode)](#toString-int) |  |
### EMF {#EMF}
```
public static int EMF
```


Aspose.Words, EMF+ Dual metafilenin EMF kısmını işler.

### EMF_PLUS {#EMF-PLUS}
```
public static int EMF_PLUS
```


Aspose.Words, EMF+ Dual metafilenin EMF+ kısmını işler.

### EMF_PLUS_WITH_FALLBACK {#EMF-PLUS-WITH-FALLBACK}
```
public static int EMF_PLUS_WITH_FALLBACK
```


Aspose.Words, EMF+ Dual metafilenin EMF+ kısmını işlemeye çalışır. Eğer bazı EMF+ kayıtları desteklenmiyorsa, Aspose.Words EMF+ Dual metafilenin EMF kısmını işler.

### length {#length}
```
public static int length
```


### fromName(String emfPlusDualRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String emfPlusDualRenderingModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| emfPlusDualRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int emfPlusDualRenderingMode) {#getName-int}
```
public static String getName(int emfPlusDualRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| emfPlusDualRenderingMode | int |  |

**Returns:**
java.lang.String
