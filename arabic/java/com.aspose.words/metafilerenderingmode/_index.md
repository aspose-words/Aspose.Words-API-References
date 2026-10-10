---
title: "MetafileRenderingMode"
linktitle: "MetafileRenderingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيف يجب على Aspose.Words عرض ملفات WMF و EMF الميتا في Java."
type: docs
weight: 467
url: /ar/java/com.aspose.words/metafilerenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingMode
```

يحدد كيفية عرض Aspose.Words لملفات WMF و EMF الوصفية.

 **Examples:** 

يعرض إضافة طريقة احتياطية إلى عرض البت ماب وتغيير نوع التحذيرات بشأن سجلات الميتافايل غير المدعومة.

```

 public void handleBinaryRasterWarnings() throws Exception {
     Document doc = new Document(getMyDir() + "WMF with image.docx");

     MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

     // Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
     // it encounters a metafile, which will require raster operations to render in the output PDF.
     metafileRenderingOptions.setEmulateRasterOperations(false);

     // Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
     metafileRenderingOptions.setRenderingMode(MetafileRenderingMode.VECTOR_WITH_FALLBACK);

     // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
     // to modify how that method converts the document to .PDF and applies the configuration
     // in our MetafileRenderingOptions object to the saving operation.
     PdfSaveOptions saveOptions = new PdfSaveOptions();
     saveOptions.setMetafileRenderingOptions(metafileRenderingOptions);

     HandleDocumentWarnings callback = new HandleDocumentWarnings();
     doc.setWarningCallback(callback);

     doc.save(getArtifactsDir() + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

     Assert.assertEquals(1, callback.mWarnings.getCount());
     Assert.assertEquals("'R2_XORPEN' binary raster operation is not supported.",
             callback.mWarnings.get(0).getDescription());
 }

 /// 
 /// Prints and collects formatting loss-related warnings that occur upon saving a document.
 /// 
 public static class HandleDocumentWarnings implements IWarningCallback {
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.MINOR_FORMATTING_LOSS) {
             System.out.println("Unsupported operation: " + info.getDescription());
             this.mWarnings.warning(info);
         }
     }

     public WarningInfoCollection mWarnings = new WarningInfoCollection();
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BITMAP](#BITMAP) | تستدعي Aspose.Words GDI+ لعرض ملف ميتافايل كصورة بت ماب ثم تحفظ الصورة في المستند الناتج. |
| [VECTOR](#VECTOR) | تقوم Aspose.Words بعرض ملف ميتافايل كرسومات متجهية. |
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | تحاول Aspose.Words عرض ملف ميتافايل كرسومات متجهية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int metafileRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int metafileRenderingMode)](#toString-int) |  |
### BITMAP {#BITMAP}
```
public static int BITMAP
```


تستدعي Aspose.Words GDI+ لعرض ملف ميتافايل كصورة بت ماب ثم تحفظ الصورة في المستند الناتج.

### VECTOR {#VECTOR}
```
public static int VECTOR
```


تقوم Aspose.Words بعرض ملف ميتافايل كرسومات متجهية.

### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


تحاول Aspose.Words عرض ملف ميتافايل كرسومات متجهية. إذا لم تستطع Aspose.Words عرض بعض سجلات الميتافايل بشكل صحيح كرسومات متجهية فإنها تعرض هذا الميتافايل كصورة بت ماب.

### length {#length}
```
public static int length
```


### fromName(String metafileRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String metafileRenderingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int metafileRenderingMode) {#getName-int}
```
public static String getName(int metafileRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int metafileRenderingMode) {#toString-int}
```
public static String toString(int metafileRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
