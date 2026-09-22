---
title: "IWarningCallback"
linktitle: "IWarningCallback"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة إذا كنت ترغب في الحصول على طريقة مخصصة خاصة بك تُستدعى لالتقاط تحذيرات فقدان الدقة التي قد تحدث أثناء تحميل المستند أو حفظه في Java."
type: docs
weight: 788
url: /ar/java/com.aspose.words/iwarningcallback/
---
```
public interface IWarningCallback
```

قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة لالتقاط تحذيرات فقدان الدقة التي قد تحدث أثناء تحميل أو حفظ المستند.

 **Examples:** 

يوضح كيفية استخدام واجهة IWarningCallback لمراقبة تحذيرات استبدال الخط.

```

 public void substitutionWarning() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Times New Roman");
     builder.writeln("Hello world!");

     FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
     doc.setWarningCallback(callback);

     // Store the current collection of font sources, which will be the default font source for every document
     // for which we do not specify a different font source.
     FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

     // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
     FontSettings.getDefaultInstance().setFontsFolder("", false);

     // When rendering the document, there will be no place to find the "Times New Roman" font.
     // This will cause a font substitution warning, which our callback will detect.
     doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarning.pdf");

     FontSettings.getDefaultInstance().setFontsSources(originalFontSources);

     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getWarningType() == WarningType.FONT_SUBSTITUTION);
     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getDescription()
             .equals("Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
 }

 private static class FontSubstitutionWarningCollector implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق للخط المفقود من مصادر الخطوط المتاحة.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo) | تستدعي Aspose.Words هذه الطريقة عندما تواجه مشكلة أثناء تحميل أو حفظ المستند قد تؤدي إلى فقدان التنسيق أو دقة البيانات. |
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo}
```
public abstract void warning(WarningInfo info)
```


تستدعي Aspose.Words هذه الطريقة عندما تواجه مشكلة أثناء تحميل أو حفظ المستند قد تؤدي إلى فقدان التنسيق أو دقة البيانات.

 **Examples:** 

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق للخط المفقود من مصادر الخطوط المتاحة.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo/) |  |

