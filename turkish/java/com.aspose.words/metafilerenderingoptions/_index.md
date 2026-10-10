---
title: "MetafileRenderingOptions"
linktitle: "MetafileRenderingOptions"
second_title: "Aspose.Words Java için"
description: "Java'da ek metafile renderleme seçeneklerini belirtmeye olanak tanır."
type: docs
weight: 468
url: /tr/java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Ek metafile render seçeneklerini belirtmeye izin verir.

Daha fazla bilgi edinmek için [ Handling Windows Metafiles ][Handling Windows Metafiles] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Desteklenmeyen metafile kayıtlarıyla ilgili uyarı türlerini değiştirme ve bitmap renderine bir yedekleme eklenmiş olduğunu gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | EMF+ Dual metafile'ların nasıl render edileceğini belirleyen bir değeri alır. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | Raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değeri alır. |
| [getEmulateRenderingToSizeOnPage()](#getEmulateRenderingToSizeOnPage) | Metafile renderlemesinin, metafilenin sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntülendiğini taklit edip etmeyeceğini belirleyen bir değeri alır. |
| [getEmulateRenderingToSizeOnPageResolution()](#getEmulateRenderingToSizeOnPageResolution) | Sayfadaki boyuta göre metafile renderleme taklidi için inç başına piksel cinsinden çözünürlüğü alır. |
| [getRenderingMode()](#getRenderingMode) | Metafile görüntülerinin nasıl render edileceğini belirleyen bir değeri alır. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | Gömülü EMF metafile'ları içeren WMF metafile'ların nasıl render edileceğini belirleyen bir değeri alır. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | Raster işlemlerinin taklidi için GDI+ kullanımını belirleyen bir değeri alır. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | EMF+ Dual metafile'ların nasıl render edileceğini belirleyen bir değeri ayarlar. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | Raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değeri ayarlar. |
| [setEmulateRenderingToSizeOnPage(boolean value)](#setEmulateRenderingToSizeOnPage-boolean) | Metafile renderlemesinin, metafilenin sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntülendiğini taklit edip etmeyeceğini belirleyen bir değeri ayarlar. |
| [setEmulateRenderingToSizeOnPageResolution(int value)](#setEmulateRenderingToSizeOnPageResolution-int) | Sayfadaki boyuta göre metafile renderleme taklidi için inç başına piksel cinsinden çözünürlüğü ayarlar. |
| [setRenderingMode(int value)](#setRenderingMode-int) | Metafile görüntülerinin nasıl render edileceğini belirleyen bir değeri ayarlar. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | Gömülü EMF metafile'ları içeren WMF metafile'ların nasıl render edileceğini belirleyen bir değeri ayarlar. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | Raster işlemlerinin taklidi için GDI+ kullanımını belirleyen bir değeri ayarlar. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


EMF+ Dual metafile'ların nasıl render edileceğini belirleyen bir değeri alır.

 **Remarks:** 

EMF+ Dual metafile'lar hem EMF+ hem de EMF bölümlerini içerir. MS Word ve GDI+ her zaman EMF+ bölümünü render eder. Aspose.Words şu anda tüm EMF+ kayıtlarını tam olarak desteklememekte ve bazı durumlarda EMF bölümünün render sonucu EMF+ bölümünün render sonucundan daha iyi görünmektedir.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır. Metafile bitmap'e render edildiğinde, EMF+ bölümü her zaman kullanılır.

Varsayılan değer [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

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

**Returns:**
int - EMF+ Dual metafile'lerin nasıl render edileceğini belirleyen bir değer. Döndürülen değer, [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/) sabitlerinden biridir.
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


Raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değeri alır.

 **Remarks:** 

Metafile'lerde belirli raster işlemleri kullanılabilir. Bunlar doğrudan vektör grafiklere render edilemez. Raster işlemlerinin taklit edilmesi, ortaya çıkan vektör grafiklerin kısmi rasterleştirilmesini gerektirir ve bu, metafile render performansını etkileyebilir.

Bu değer true olarak ayarlandığında, Aspose.Words raster işlemlerini taklit eder. Oluşan çıktı kısmen rasterleştirilebilir ve performans daha yavaş olabilir.

Bu değer false olarak ayarlandığında, Aspose.Words raster işlemlerini taklit etmez. Aspose.Words bir metafile içinde raster işlemiyle karşılaştığında, işletim sistemini kullanarak metafile'i bir bitmap olarak render etmeye geri döner.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer  true .

 **Examples:** 

Desteklenmeyen metafile kayıtlarıyla ilgili uyarı türlerini değiştirme ve bitmap renderine bir yedekleme eklenmiş olduğunu gösterir.

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
boolean - Raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değer.
### getEmulateRenderingToSizeOnPage() {#getEmulateRenderingToSizeOnPage}
```
public boolean getEmulateRenderingToSizeOnPage()
```


Metafile renderlemesinin, metafilenin sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntülendiğini taklit edip etmeyeceğini belirleyen bir değeri alır.

 **Remarks:** 

Metafile'ler MS Word'de görüntülendiğinde, bazı grafikler gerçek metafile boyutuna piksel olarak göre ölçeklenebilir. Yani, yakınlaştırma bile metafile görüntüsünü etkileyebilir.

Bu değer true olarak ayarlandığında, Aspose.Words sayfadaki metafile boyutuna göre render etmeyi taklit eder. Piksel cinsinden boyut, sayfadaki metafile boyutundan ve belirtilen [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int) değerlerinden hesaplanır.

Bu değer false olarak ayarlandığında, Aspose.Words metafile render'ını piksel cinsinden varsayılan boyutuna taklit eder.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer  true .

 **Examples:** 

Metafile'nin sayfadaki boyuta göre nasıl görüntüleneceğini gösterir.

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
boolean - Metafile render'ının, metafile'yi sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntüleyeceğini taklit edip etmeyeceğini belirleyen bir değer.
### getEmulateRenderingToSizeOnPageResolution() {#getEmulateRenderingToSizeOnPageResolution}
```
public int getEmulateRenderingToSizeOnPageResolution()
```


Sayfadaki boyuta göre metafile renderleme taklidi için inç başına piksel cinsinden çözünürlüğü alır.

 **Remarks:** 

Bu seçenek yalnızca [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) true olarak ayarlandığında kullanılır.

Varsayılan değer 96'dır. Bu, varsayılan bir görüntüleme çözünürlüğüdür. Yani, metafile render'ı MS Word'de %100 yakınlaştırma faktörüyle metafile'nin görüntülenmesini taklit edecektir.

 **Examples:** 

Metafile'nin sayfadaki boyuta göre nasıl görüntüleneceğini gösterir.

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
int - Sayfadaki boyuta göre metafile render taklidi için inç başına piksel çözünürlüğü.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


Metafile görüntülerinin nasıl render edileceğini belirleyen bir değeri alır.

 **Remarks:** 

Varsayılan değer kaydetme formatına bağlıdır. Görüntüler için [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP) değeridir. Diğer formatlar için ise [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK) değeridir.

 **Examples:** 

Desteklenmeyen metafile kayıtlarıyla ilgili uyarı türlerini değiştirme ve bitmap renderine bir yedekleme eklenmiş olduğunu gösterir.

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
int - Metafile görüntülerinin nasıl render edileceğini belirleyen bir değer. Döndürülen değer, [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/) sabitlerinden biridir.
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


Gömülü EMF metafile'ları içeren WMF metafile'ların nasıl render edileceğini belirleyen bir değeri alır.

 **Remarks:** 

WMF metafile'leri gömülü EMF verisi içerebilir. MS Word çoğu durumda gömülü EMF verisini kullanır. GDI+ ise her zaman WMF verisini kullanır.

Bu değer true olarak ayarlandığında, Aspose.Words render sırasında gömülü EMF verisini kullanır.

Bu değer false olarak ayarlandığında, Aspose.Words render sırasında WMF verisini kullanır.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır. Metafile bitmap olarak render edildiğinde ise WMF verisi her zaman kullanılır.

Varsayılan değer  true .

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

**Returns:**
boolean - Gömülü EMF metafile'li WMF metafile'lerinin nasıl render edileceğini belirleyen bir değer.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


Raster işlemlerinin taklidi için GDI+ kullanımını belirleyen bir değeri alır.

 **Remarks:** 

Windows GDI+ kütüphanesi raster işlemleri taklit etmek için kullanılabilir. Aspose.Words'ün kendi taklidine kıyasla tüm raster işlemlerini destekler, ancak bazı durumlarda performans daha yavaş olabilir.

Bu değer true olarak ayarlandığında, Aspose.Words raster işlemleri taklidi için GDI+ kullanır.

Bu değer false olarak ayarlandığında, Aspose.Words raster işlemleri taklidi için kendi uygulamasını kullanır.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer  false  dır.

 **Examples:** 

Windows Metafile görüntüleri içeren belgeleri diğer görüntü formatlarına kaydederken işleme modunun nasıl ayarlanacağını gösterir.

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
boolean - GDI+ kullanılarak raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değer.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


EMF+ Dual metafile'ların nasıl render edileceğini belirleyen bir değeri ayarlar.

 **Remarks:** 

EMF+ Dual metafile'lar hem EMF+ hem de EMF bölümlerini içerir. MS Word ve GDI+ her zaman EMF+ bölümünü render eder. Aspose.Words şu anda tüm EMF+ kayıtlarını tam olarak desteklememekte ve bazı durumlarda EMF bölümünün render sonucu EMF+ bölümünün render sonucundan daha iyi görünmektedir.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır. Metafile bitmap'e render edildiğinde, EMF+ bölümü her zaman kullanılır.

Varsayılan değer [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | EMF+ Dual metafilelerin nasıl işleneceğini belirleyen bir değer. Değer, [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/) sabitlerinden biri olmalıdır. |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


Raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değeri ayarlar.

 **Remarks:** 

Metafile'lerde belirli raster işlemleri kullanılabilir. Bunlar doğrudan vektör grafiklere render edilemez. Raster işlemlerinin taklit edilmesi, ortaya çıkan vektör grafiklerin kısmi rasterleştirilmesini gerektirir ve bu, metafile render performansını etkileyebilir.

Bu değer true olarak ayarlandığında, Aspose.Words raster işlemlerini taklit eder. Oluşan çıktı kısmen rasterleştirilebilir ve performans daha yavaş olabilir.

Bu değer false olarak ayarlandığında, Aspose.Words raster işlemlerini taklit etmez. Aspose.Words bir metafile içinde raster işlemiyle karşılaştığında, işletim sistemini kullanarak metafile'i bir bitmap olarak render etmeye geri döner.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer  true .

 **Examples:** 

Desteklenmeyen metafile kayıtlarıyla ilgili uyarı türlerini değiştirme ve bitmap renderine bir yedekleme eklenmiş olduğunu gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Raster işlemlerinin taklit edilip edilmeyeceğini belirleyen bir değer. |

### setEmulateRenderingToSizeOnPage(boolean value) {#setEmulateRenderingToSizeOnPage-boolean}
```
public void setEmulateRenderingToSizeOnPage(boolean value)
```


Metafile renderlemesinin, metafilenin sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntülendiğini taklit edip etmeyeceğini belirleyen bir değeri ayarlar.

 **Remarks:** 

Metafile'ler MS Word'de görüntülendiğinde, bazı grafikler gerçek metafile boyutuna piksel olarak göre ölçeklenebilir. Yani, yakınlaştırma bile metafile görüntüsünü etkileyebilir.

Bu değer true olarak ayarlandığında, Aspose.Words sayfadaki metafile boyutuna göre render etmeyi taklit eder. Piksel cinsinden boyut, sayfadaki metafile boyutundan ve belirtilen [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int) değerlerinden hesaplanır.

Bu değer false olarak ayarlandığında, Aspose.Words metafile render'ını piksel cinsinden varsayılan boyutuna taklit eder.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer  true .

 **Examples:** 

Metafile'nin sayfadaki boyuta göre nasıl görüntüleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Metafile işleme, metafilenin sayfadaki boyuta göre mi yoksa varsayılan boyutunda mı görüntüleneceğini taklit edeceğini belirleyen bir değer. |

### setEmulateRenderingToSizeOnPageResolution(int value) {#setEmulateRenderingToSizeOnPageResolution-int}
```
public void setEmulateRenderingToSizeOnPageResolution(int value)
```


Sayfadaki boyuta göre metafile renderleme taklidi için inç başına piksel cinsinden çözünürlüğü ayarlar.

 **Remarks:** 

Bu seçenek yalnızca [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) true olarak ayarlandığında kullanılır.

Varsayılan değer 96'dır. Bu, varsayılan bir görüntüleme çözünürlüğüdür. Yani, metafile render'ı MS Word'de %100 yakınlaştırma faktörüyle metafile'nin görüntülenmesini taklit edecektir.

 **Examples:** 

Metafile'nin sayfadaki boyuta göre nasıl görüntüleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Sayfadaki boyuta göre metafile işleme taklidi için inç başına piksel cinsinden çözünürlük. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


Metafile görüntülerinin nasıl render edileceğini belirleyen bir değeri ayarlar.

 **Remarks:** 

Varsayılan değer kaydetme formatına bağlıdır. Görüntüler için [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP) değeridir. Diğer formatlar için ise [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK) değeridir.

 **Examples:** 

Desteklenmeyen metafile kayıtlarıyla ilgili uyarı türlerini değiştirme ve bitmap renderine bir yedekleme eklenmiş olduğunu gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Metafile görüntülerinin nasıl işleneceğini belirleyen bir değer. Değer, [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/) sabitlerinden biri olmalıdır. |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Gömülü EMF metafile'ları içeren WMF metafile'ların nasıl render edileceğini belirleyen bir değeri ayarlar.

 **Remarks:** 

WMF metafile'leri gömülü EMF verisi içerebilir. MS Word çoğu durumda gömülü EMF verisini kullanır. GDI+ ise her zaman WMF verisini kullanır.

Bu değer true olarak ayarlandığında, Aspose.Words render sırasında gömülü EMF verisini kullanır.

Bu değer false olarak ayarlandığında, Aspose.Words render sırasında WMF verisini kullanır.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır. Metafile bitmap olarak render edildiğinde ise WMF verisi her zaman kullanılır.

Varsayılan değer  true .

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Gömülü EMF metafileleri içeren WMF metafilelerin nasıl işleneceğini belirleyen bir değer. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


Raster işlemlerinin taklidi için GDI+ kullanımını belirleyen bir değeri ayarlar.

 **Remarks:** 

Windows GDI+ kütüphanesi raster işlemleri taklit etmek için kullanılabilir. Aspose.Words'ün kendi taklidine kıyasla tüm raster işlemlerini destekler, ancak bazı durumlarda performans daha yavaş olabilir.

Bu değer true olarak ayarlandığında, Aspose.Words raster işlemleri taklidi için GDI+ kullanır.

Bu değer false olarak ayarlandığında, Aspose.Words raster işlemleri taklidi için kendi uygulamasını kullanır.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer  false  dır.

 **Examples:** 

Windows Metafile görüntüleri içeren belgeleri diğer görüntü formatlarına kaydederken işleme modunun nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Raster işlemlerinin taklit edilmesi için GDI+ kullanılıp kullanılmayacağını belirleyen bir değer. |

