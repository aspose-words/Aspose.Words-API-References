---
title: "MetafileRenderingOptions"
linktitle: "MetafileRenderingOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات إضافية لتصيير ملفات الميتا في Java."
type: docs
weight: 468
url: /ar/java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

يسمح بتحديد خيارات إضافية لعرض ملفات الميتا.

لمزيد من المعلومات، زر مقالة الوثائق [ Handling Windows Metafiles ][Handling Windows Metafiles].

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


[Handling Windows Metafiles]: https://docs.aspose.com/words/java/handling-windows-metafiles/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | يحصل على قيمة تحدد كيفية تصيير ملفات EMF+ Dual. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | يحصل على قيمة تحدد ما إذا كان يجب محاكاة عمليات الرستر أم لا. |
| [getEmulateRenderingToSizeOnPage()](#getEmulateRenderingToSizeOnPage) | يحصل على قيمة تحدد ما إذا كان تصيير ملف الميتا يحاكي عرض الملف وفقًا لحجمه على الصفحة أم يعرضه بحجمه الافتراضي. |
| [getEmulateRenderingToSizeOnPageResolution()](#getEmulateRenderingToSizeOnPageResolution) | يحصل على الدقة بوحدات البكسل لكل بوصة لمحاكاة تصيير ملف الميتا إلى الحجم على الصفحة. |
| [getRenderingMode()](#getRenderingMode) | يحصل على قيمة تحدد كيفية تصيير صور ملفات الميتا. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | يحصل على قيمة تحدد كيفية تصيير ملفات WMF التي تحتوي على ملفات EMF مدمجة. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | يحصل على قيمة تحدد ما إذا كان يجب استخدام GDI+ لمحاكاة عمليات الرستر أم لا. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | يضبط قيمة تحدد كيفية تصيير ملفات EMF+ Dual. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | يضبط قيمة تحدد ما إذا كان يجب محاكاة عمليات الرستر أم لا. |
| [setEmulateRenderingToSizeOnPage(boolean value)](#setEmulateRenderingToSizeOnPage-boolean) | يضبط قيمة تحدد ما إذا كان تصيير ملف الميتا يحاكي عرض الملف وفقًا لحجمه على الصفحة أم يعرضه بحجمه الافتراضي. |
| [setEmulateRenderingToSizeOnPageResolution(int value)](#setEmulateRenderingToSizeOnPageResolution-int) | يضبط الدقة بوحدات البكسل لكل بوصة لمحاكاة تصيير ملف الميتا إلى الحجم على الصفحة. |
| [setRenderingMode(int value)](#setRenderingMode-int) | يضبط قيمة تحدد كيفية تصيير صور ملفات الميتا. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | يضبط قيمة تحدد كيفية تصيير ملفات WMF التي تحتوي على ملفات EMF مدمجة. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | يضبط قيمة تحدد ما إذا كان يجب استخدام GDI+ لمحاكاة عمليات الرستر أم لا. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


يحصل على قيمة تحدد كيفية تصيير ملفات EMF+ Dual.

 **Remarks:** 

ملفات EMF+ Dual تحتوي على كل من أجزاء EMF+ و EMF. برنامج MS Word و GDI+ دائمًا ما يصيران الجزء EMF+. حاليًا لا يدعم Aspose.Words جميع سجلات EMF+ بشكل كامل، وفي بعض الحالات يبدو نتيجة تصيير جزء EMF أفضل من نتيجة تصيير جزء EMF+.

يُستخدم هذا الخيار فقط عندما يتم تصيير ملف الميتا كرسومات متجهة. عندما يتم تصيير ملف الميتا إلى صورة نقطية، يُستخدم دائمًا الجزء EMF+.

القيمة الافتراضية هي [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

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

**Returns:**
int - قيمة تحدد كيفية عرض ملفات EMF+ Dual. القيمة المرجعة هي واحدة من ثوابت [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/).
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


يحصل على قيمة تحدد ما إذا كان يجب محاكاة عمليات الرستر أم لا.

 **Remarks:** 

يمكن استخدام عمليات نقطية محددة في ملفات الميتافايل. لا يمكن عرضها مباشرةً كرسومات متجهة. يتطلب محاكاة العمليات النقطية تمثيلًا جزئيًا للرسومات المتجهة الناتجة مما قد يؤثر على أداء عرض الميتافايل.

عند ضبط هذه القيمة على true، تقوم Aspose.Words بمحاكاة العمليات النقطية. قد يكون الناتج المولّد مُمثلاً جزئيًا وقد يكون الأداء أبطأ.

عند ضبط هذه القيمة على false، لا تقوم Aspose.Words بمحاكاة العمليات النقطية. عندما تواجه Aspose.Words عملية نقطية في ملف ميتافايل، فإنها تلجأ إلى عرض الملف كصورة نقطية باستخدام نظام التشغيل.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة.

القيمة الافتراضية هي  true .

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

**Returns:**
boolean - قيمة تحدد ما إذا كان يجب محاكاة العمليات النقطية أم لا.
### getEmulateRenderingToSizeOnPage() {#getEmulateRenderingToSizeOnPage}
```
public boolean getEmulateRenderingToSizeOnPage()
```


يحصل على قيمة تحدد ما إذا كان تصيير ملف الميتا يحاكي عرض الملف وفقًا لحجمه على الصفحة أم يعرضه بحجمه الافتراضي.

 **Remarks:** 

عند عرض ملفات الميتافايل في MS Word، قد يتم تحجيم بعض الرسومات وفقًا لحجم الميتافايل الفعلي بالبكسل. أي أن التكبير قد يؤثر أيضًا على عرض الميتافايل.

عند ضبط هذه القيمة على true، تقوم Aspose.Words بمحاكاة العرض وفقًا لحجم الميتافايل على الصفحة. يتم حساب الحجم بالبكسل من حجم الميتافايل على الصفحة والـ [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

عند ضبط هذه القيمة على false، تقوم Aspose.Words بمحاكاة عرض الميتافايل بحجمه الافتراضي بالبكسل.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة.

القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية عرض الميتافايل وفقًا لحجمه على الصفحة.

```

 Document doc = new Document(getMyDir() + "WMF with text.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "EmulateRenderingToSizeOnPage" property to "true"
 // to emulate rendering according to the metafile size on page.
 // Set the "EmulateRenderingToSizeOnPage" property to "false"
 // to emulate metafile rendering to its default size in pixels.
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPage(renderToSize);
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPageResolution(50);

 doc.save(getArtifactsDir() + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
 
```

**Returns:**
boolean - قيمة تحدد ما إذا كان عرض الميتافايل يحاكي عرضه وفقًا لحجمه على الصفحة أم عرضه بحجمه الافتراضي.
### getEmulateRenderingToSizeOnPageResolution() {#getEmulateRenderingToSizeOnPageResolution}
```
public int getEmulateRenderingToSizeOnPageResolution()
```


يحصل على الدقة بوحدات البكسل لكل بوصة لمحاكاة تصيير ملف الميتا إلى الحجم على الصفحة.

 **Remarks:** 

يُستخدم هذا الخيار فقط عندما تكون الدوال [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) مضبوطة على true.

القيمة الافتراضية هي 96. هذه هي دقة العرض الافتراضية. أي أن عرض الميتافايل سيحاكي عرضه في MS Word بنسبة تكبير 100٪.

 **Examples:** 

يوضح كيفية عرض الميتافايل وفقًا لحجمه على الصفحة.

```

 Document doc = new Document(getMyDir() + "WMF with text.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "EmulateRenderingToSizeOnPage" property to "true"
 // to emulate rendering according to the metafile size on page.
 // Set the "EmulateRenderingToSizeOnPage" property to "false"
 // to emulate metafile rendering to its default size in pixels.
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPage(renderToSize);
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPageResolution(50);

 doc.save(getArtifactsDir() + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
 
```

**Returns:**
int - الدقة بالبكسل لكل بوصة لمحاكاة عرض الميتافايل بحجمه على الصفحة.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


يحصل على قيمة تحدد كيفية تصيير صور ملفات الميتا.

 **Remarks:** 

القيمة الافتراضية تعتمد على تنسيق الحفظ. بالنسبة للصور تكون [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). بالنسبة للتنسيقات الأخرى تكون [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

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

**Returns:**
int - قيمة تحدد كيفية عرض صور الميتافايل. القيمة المرجعة هي واحدة من ثوابت [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/).
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


يحصل على قيمة تحدد كيفية تصيير ملفات WMF التي تحتوي على ملفات EMF مدمجة.

 **Remarks:** 

قد تحتوي ملفات WMF على بيانات EMF مدمجة. في معظم الحالات يستخدم MS Word بيانات EMF المدمجة. دائمًا يستخدم GDI+ بيانات WMF.

عند ضبط هذه القيمة على true، تستخدم Aspose.Words بيانات EMF المدمجة عند العرض.

عند ضبط هذه القيمة على false، تستخدم Aspose.Words بيانات WMF عند العرض.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة. عندما يُعرض الميتافايل كصورة نقطية، تُستخدم بيانات WMF دائمًا.

القيمة الافتراضية هي  true .

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

**Returns:**
boolean - قيمة تحدد كيفية عرض ملفات WMF التي تحتوي على ملفات EMF مدمجة.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


يحصل على قيمة تحدد ما إذا كان يجب استخدام GDI+ لمحاكاة عمليات الرستر أم لا.

 **Remarks:** 

يمكن استخدام مكتبة Windows GDI+ لمحاكاة العمليات النقطية. فهي توفر دعمًا لجميع العمليات النقطية مقارنةً بمحاكاة Aspose.Words الخاصة، لكن الأداء قد يكون أبطأ في بعض الحالات.

عند ضبط هذه القيمة على true، تستخدم Aspose.Words مكتبة GDI+ لمحاكاة العمليات النقطية.

عند ضبط هذه القيمة على false، تستخدم Aspose.Words تنفيذها الخاص لمحاكاة العمليات النقطية.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية تعيين وضع العرض عند حفظ المستندات التي تحتوي على صور Windows Metafile إلى صيغ صور أخرى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Windows MetaFile.wmf");

 // When we save the document as an image, we can pass a SaveOptions object to
 // determine how the saving operation will process Windows Metafiles in the document.
 // If we set the "RenderingMode" property to "MetafileRenderingMode.Vector",
 // or "MetafileRenderingMode.VectorWithFallback", we will render all metafiles as vector graphics.
 // If we set the "RenderingMode" property to "MetafileRenderingMode.Bitmap", we will render all metafiles as bitmaps.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 options.getMetafileRenderingOptions().setRenderingMode(metafileRenderingMode);
 // Aspose.Words uses GDI+ for raster operations emulation, when value is set to true.
 options.getMetafileRenderingOptions().setUseGdiRasterOperationsEmulation(true);

 doc.save(getArtifactsDir() + "ImageSaveOptions.WindowsMetaFile.png", options);
 
```

**Returns:**
boolean - قيمة تحدد ما إذا كان يجب استخدام GDI+ لمحاكاة عمليات النقطية أم لا.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


يضبط قيمة تحدد كيفية تصيير ملفات EMF+ Dual.

 **Remarks:** 

ملفات EMF+ Dual تحتوي على كل من أجزاء EMF+ و EMF. برنامج MS Word و GDI+ دائمًا ما يصيران الجزء EMF+. حاليًا لا يدعم Aspose.Words جميع سجلات EMF+ بشكل كامل، وفي بعض الحالات يبدو نتيجة تصيير جزء EMF أفضل من نتيجة تصيير جزء EMF+.

يُستخدم هذا الخيار فقط عندما يتم تصيير ملف الميتا كرسومات متجهة. عندما يتم تصيير ملف الميتا إلى صورة نقطية، يُستخدم دائمًا الجزء EMF+.

القيمة الافتراضية هي [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | قيمة تحدد كيفية عرض ملفات EMF+ Dual. يجب أن تكون القيمة واحدة من ثوابت [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/). |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


يضبط قيمة تحدد ما إذا كان يجب محاكاة عمليات الرستر أم لا.

 **Remarks:** 

يمكن استخدام عمليات نقطية محددة في ملفات الميتافايل. لا يمكن عرضها مباشرةً كرسومات متجهة. يتطلب محاكاة العمليات النقطية تمثيلًا جزئيًا للرسومات المتجهة الناتجة مما قد يؤثر على أداء عرض الميتافايل.

عند ضبط هذه القيمة على true، تقوم Aspose.Words بمحاكاة العمليات النقطية. قد يكون الناتج المولّد مُمثلاً جزئيًا وقد يكون الأداء أبطأ.

عند ضبط هذه القيمة على false، لا تقوم Aspose.Words بمحاكاة العمليات النقطية. عندما تواجه Aspose.Words عملية نقطية في ملف ميتافايل، فإنها تلجأ إلى عرض الملف كصورة نقطية باستخدام نظام التشغيل.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة.

القيمة الافتراضية هي  true .

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تحدد ما إذا كان يجب محاكاة عمليات النقطية أم لا. |

### setEmulateRenderingToSizeOnPage(boolean value) {#setEmulateRenderingToSizeOnPage-boolean}
```
public void setEmulateRenderingToSizeOnPage(boolean value)
```


يضبط قيمة تحدد ما إذا كان تصيير ملف الميتا يحاكي عرض الملف وفقًا لحجمه على الصفحة أم يعرضه بحجمه الافتراضي.

 **Remarks:** 

عند عرض ملفات الميتافايل في MS Word، قد يتم تحجيم بعض الرسومات وفقًا لحجم الميتافايل الفعلي بالبكسل. أي أن التكبير قد يؤثر أيضًا على عرض الميتافايل.

عند ضبط هذه القيمة على true، تقوم Aspose.Words بمحاكاة العرض وفقًا لحجم الميتافايل على الصفحة. يتم حساب الحجم بالبكسل من حجم الميتافايل على الصفحة والـ [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

عند ضبط هذه القيمة على false، تقوم Aspose.Words بمحاكاة عرض الميتافايل بحجمه الافتراضي بالبكسل.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة.

القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية عرض الميتافايل وفقًا لحجمه على الصفحة.

```

 Document doc = new Document(getMyDir() + "WMF with text.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "EmulateRenderingToSizeOnPage" property to "true"
 // to emulate rendering according to the metafile size on page.
 // Set the "EmulateRenderingToSizeOnPage" property to "false"
 // to emulate metafile rendering to its default size in pixels.
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPage(renderToSize);
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPageResolution(50);

 doc.save(getArtifactsDir() + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تحدد ما إذا كان عرض ملف الميتا يحاكي عرض الملف وفقًا لحجمه على الصفحة أم يعرضه بحجمه الافتراضي. |

### setEmulateRenderingToSizeOnPageResolution(int value) {#setEmulateRenderingToSizeOnPageResolution-int}
```
public void setEmulateRenderingToSizeOnPageResolution(int value)
```


يضبط الدقة بوحدات البكسل لكل بوصة لمحاكاة تصيير ملف الميتا إلى الحجم على الصفحة.

 **Remarks:** 

يُستخدم هذا الخيار فقط عندما تكون الدوال [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) مضبوطة على true.

القيمة الافتراضية هي 96. هذه هي دقة العرض الافتراضية. أي أن عرض الميتافايل سيحاكي عرضه في MS Word بنسبة تكبير 100٪.

 **Examples:** 

يوضح كيفية عرض الميتافايل وفقًا لحجمه على الصفحة.

```

 Document doc = new Document(getMyDir() + "WMF with text.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "EmulateRenderingToSizeOnPage" property to "true"
 // to emulate rendering according to the metafile size on page.
 // Set the "EmulateRenderingToSizeOnPage" property to "false"
 // to emulate metafile rendering to its default size in pixels.
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPage(renderToSize);
 saveOptions.getMetafileRenderingOptions().setEmulateRenderingToSizeOnPageResolution(50);

 doc.save(getArtifactsDir() + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | الدقة بوحدات البكسل لكل بوصة لمحاكاة عرض ملف الميتا إلى الحجم على الصفحة. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


يضبط قيمة تحدد كيفية تصيير صور ملفات الميتا.

 **Remarks:** 

القيمة الافتراضية تعتمد على تنسيق الحفظ. بالنسبة للصور تكون [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). بالنسبة للتنسيقات الأخرى تكون [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | قيمة تحدد كيفية عرض صور ملفات الميتا. يجب أن تكون القيمة واحدة من ثوابت [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/). |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


يضبط قيمة تحدد كيفية تصيير ملفات WMF التي تحتوي على ملفات EMF مدمجة.

 **Remarks:** 

قد تحتوي ملفات WMF على بيانات EMF مدمجة. في معظم الحالات يستخدم MS Word بيانات EMF المدمجة. دائمًا يستخدم GDI+ بيانات WMF.

عند ضبط هذه القيمة على true، تستخدم Aspose.Words بيانات EMF المدمجة عند العرض.

عند ضبط هذه القيمة على false، تستخدم Aspose.Words بيانات WMF عند العرض.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة. عندما يُعرض الميتافايل كصورة نقطية، تُستخدم بيانات WMF دائمًا.

القيمة الافتراضية هي  true .

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تحدد كيفية عرض ملفات WMF التي تحتوي على ملفات EMF مدمجة. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


يضبط قيمة تحدد ما إذا كان يجب استخدام GDI+ لمحاكاة عمليات الرستر أم لا.

 **Remarks:** 

يمكن استخدام مكتبة Windows GDI+ لمحاكاة العمليات النقطية. فهي توفر دعمًا لجميع العمليات النقطية مقارنةً بمحاكاة Aspose.Words الخاصة، لكن الأداء قد يكون أبطأ في بعض الحالات.

عند ضبط هذه القيمة على true، تستخدم Aspose.Words مكتبة GDI+ لمحاكاة العمليات النقطية.

عند ضبط هذه القيمة على false، تستخدم Aspose.Words تنفيذها الخاص لمحاكاة العمليات النقطية.

يُستخدم هذا الخيار فقط عندما يتم عرض الميتافايل كرسومات متجهة.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية تعيين وضع العرض عند حفظ المستندات التي تحتوي على صور Windows Metafile إلى صيغ صور أخرى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Windows MetaFile.wmf");

 // When we save the document as an image, we can pass a SaveOptions object to
 // determine how the saving operation will process Windows Metafiles in the document.
 // If we set the "RenderingMode" property to "MetafileRenderingMode.Vector",
 // or "MetafileRenderingMode.VectorWithFallback", we will render all metafiles as vector graphics.
 // If we set the "RenderingMode" property to "MetafileRenderingMode.Bitmap", we will render all metafiles as bitmaps.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 options.getMetafileRenderingOptions().setRenderingMode(metafileRenderingMode);
 // Aspose.Words uses GDI+ for raster operations emulation, when value is set to true.
 options.getMetafileRenderingOptions().setUseGdiRasterOperationsEmulation(true);

 doc.save(getArtifactsDir() + "ImageSaveOptions.WindowsMetaFile.png", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تحدد ما إذا كان يجب استخدام GDI+ لمحاكاة عمليات النقطية أم لا. |

