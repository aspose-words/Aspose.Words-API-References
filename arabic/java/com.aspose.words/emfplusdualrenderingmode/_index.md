---
title: "EmfPlusDualRenderingMode"
linktitle: "EmfPlusDualRenderingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية قيام Aspose.Words بتصيير ملفات EMF Dual في Java."
type: docs
weight: 186
url: /ar/java/com.aspose.words/emfplusdualrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class EmfPlusDualRenderingMode
```

يحدد كيفية قيام Aspose.Words بعرض ملفات EMF+ Dual.

 **Examples:** 

يوضح كيفية تكوين خيارات التصيير المتعلقة بـ Enhanced Windows Metafile عند الحفظ إلى PDF.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [EMF](#EMF) | يقوم Aspose.Words بتصيير جزء EMF من ملف EMF+ Dual. |
| [EMF_PLUS](#EMF-PLUS) | يقوم Aspose.Words بتصيير جزء EMF+ من ملف EMF+ Dual. |
| [EMF_PLUS_WITH_FALLBACK](#EMF-PLUS-WITH-FALLBACK) | يحاول Aspose.Words تصيير جزء EMF+ من ملف EMF+ Dual. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String emfPlusDualRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int emfPlusDualRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emfPlusDualRenderingMode)](#toString-int) |  |
### EMF {#EMF}
```
public static int EMF
```


يقوم Aspose.Words بتصيير جزء EMF من ملف EMF+ Dual.

### EMF_PLUS {#EMF-PLUS}
```
public static int EMF_PLUS
```


يقوم Aspose.Words بتصيير جزء EMF+ من ملف EMF+ Dual.

### EMF_PLUS_WITH_FALLBACK {#EMF-PLUS-WITH-FALLBACK}
```
public static int EMF_PLUS_WITH_FALLBACK
```


يحاول Aspose.Words تصيير جزء EMF+ من ملف EMF+ Dual. إذا لم يتم دعم بعض سجلات EMF+، فإن Aspose.Words يقوم بتصيير جزء EMF من ملف EMF+ Dual.

### length {#length}
```
public static int length
```


### fromName(String emfPlusDualRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String emfPlusDualRenderingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| emfPlusDualRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int emfPlusDualRenderingMode) {#getName-int}
```
public static String getName(int emfPlusDualRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| emfPlusDualRenderingMode | int |  |

**Returns:**
java.lang.String
