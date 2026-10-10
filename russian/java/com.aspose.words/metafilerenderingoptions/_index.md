---
title: "MetafileRenderingOptions"
linktitle: "MetafileRenderingOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет указать дополнительные параметры рендеринга метафайлов в Java."
type: docs
weight: 468
url: /ru/java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Позволяет указать дополнительные параметры отображения метафайлов.

Чтобы узнать больше, посетите статью документации [ Handling Windows Metafiles ][Handling Windows Metafiles].

 **Examples:** 

Показывает, что добавлен резервный режим рендеринга в bitmap и изменён тип предупреждений о неподдерживаемых записях метафайла.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | Получает значение, определяющее, как должны рендериться EMF+ Dual метафайлы. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | Получает значение, определяющее, следует ли эмулировать растровые операции. |
| [getEmulateRenderingToSizeOnPage()](#getEmulateRenderingToSizeOnPage) | Получает значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию. |
| [getEmulateRenderingToSizeOnPageResolution()](#getEmulateRenderingToSizeOnPageResolution) | Получает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла к размеру на странице. |
| [getRenderingMode()](#getRenderingMode) | Получает значение, определяющее, как должны рендериться изображения метафайлов. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | Получает значение, определяющее, как должны рендериться WMF метафайлы с вложенными EMF метафайлами. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | Получает значение, определяющее, следует ли использовать GDI+ для эмуляции растровых операций. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | Устанавливает значение, определяющее, как должны рендериться EMF+ Dual метафайлы. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | Устанавливает значение, определяющее, следует ли эмулировать растровые операции. |
| [setEmulateRenderingToSizeOnPage(boolean value)](#setEmulateRenderingToSizeOnPage-boolean) | Устанавливает значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию. |
| [setEmulateRenderingToSizeOnPageResolution(int value)](#setEmulateRenderingToSizeOnPageResolution-int) | Устанавливает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла к размеру на странице. |
| [setRenderingMode(int value)](#setRenderingMode-int) | Устанавливает значение, определяющее, как должны рендериться изображения метафайлов. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | Устанавливает значение, определяющее, как должны рендериться WMF метафайлы с вложенными EMF метафайлами. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | Устанавливает значение, определяющее, следует ли использовать GDI+ для эмуляции растровых операций. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


Получает значение, определяющее, как должны рендериться EMF+ Dual метафайлы.

 **Remarks:** 

EMF+ Dual метафайлы содержат как части EMF+, так и части EMF. MS Word и GDI+ всегда рендерят часть EMF+. Aspose.Words в настоящее время не полностью поддерживает все записи EMF+ и в некоторых случаях результат рендеринга части EMF выглядит лучше, чем результат рендеринга части EMF+.

Этот параметр используется только когда метафайл рендерится как векторная графика. Когда метафайл рендерится в bitmap, часть EMF+ всегда используется.

Значение по умолчанию — [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

 **Examples:** 

Показывает, как настроить параметры рендеринга, связанные с Enhanced Windows Metafile, при сохранении в PDF.

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
int - Значение, определяющее, как должны отображаться EMF+ Dual метафайлы. Возвращаемое значение является одной из констант [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/).
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


Получает значение, определяющее, следует ли эмулировать растровые операции.

 **Remarks:** 

В метафайлах могут использоваться специфические растровые операции. Их нельзя отобразить напрямую в векторную графику. Эмуляция растровых операций требует частичной растеризации полученной векторной графики, что может повлиять на производительность рендеринга метафайла.

Когда это значение установлено в  true , Aspose.Words эмулирует растровые операции. Полученный вывод может быть частично растеризован, и производительность может быть ниже.

Когда это значение установлено в  false , Aspose.Words не эмулирует растровые операции. Когда Aspose.Words встречает растровую операцию в метафайле, он переходит к рендерингу метафайла в bitmap, используя операционную систему.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию —  true .

 **Examples:** 

Показывает, что добавлен резервный режим рендеринга в bitmap и изменён тип предупреждений о неподдерживаемых записях метафайла.

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
boolean - Значение, определяющее, следует ли эмулировать растровые операции.
### getEmulateRenderingToSizeOnPage() {#getEmulateRenderingToSizeOnPage}
```
public boolean getEmulateRenderingToSizeOnPage()
```


Получает значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию.

 **Remarks:** 

Когда метафайлы отображаются в MS Word, некоторые графические элементы могут масштабироваться в соответствии с фактическим размером метафайла в пикселях. То есть даже масштабирование может влиять на отображение метафайла.

Когда это значение установлено в  true , Aspose.Words эмулирует рендеринг в соответствии с размером метафайла на странице. Размер в пикселях рассчитывается из размера метафайла на странице и указанного [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Когда это значение установлено в  false , Aspose.Words эмулирует рендеринг метафайла до его стандартного размера в пикселях.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию —  true .

 **Examples:** 

Показывает, как отображать метафайл в соответствии с размером на странице.

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
boolean - Значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его стандартном размере.
### getEmulateRenderingToSizeOnPageResolution() {#getEmulateRenderingToSizeOnPageResolution}
```
public int getEmulateRenderingToSizeOnPageResolution()
```


Получает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла к размеру на странице.

 **Remarks:** 

Эта опция используется только когда [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) установлен в  true .

Значение по умолчанию — 96. Это стандартное разрешение отображения. То есть рендеринг метафайла будет эмулировать отображение метафайла в MS Word с коэффициентом масштабирования 100%.

 **Examples:** 

Показывает, как отображать метафайл в соответствии с размером на странице.

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
int - Разрешение в пикселях на дюйм для эмуляции рендеринга метафайла до размера на странице.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


Получает значение, определяющее, как должны рендериться изображения метафайлов.

 **Remarks:** 

Значение по умолчанию зависит от формата сохранения. Для изображений это [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Для других форматов это [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Показывает, что добавлен резервный режим рендеринга в bitmap и изменён тип предупреждений о неподдерживаемых записях метафайла.

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
int - Значение, определяющее, как должны рендериться изображения метафайлов. Возвращаемое значение является одной из констант [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/).
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


Получает значение, определяющее, как должны рендериться WMF метафайлы с вложенными EMF метафайлами.

 **Remarks:** 

WMF‑метафайлы могут содержать встроенные данные EMF. В большинстве случаев MS Word использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда это значение установлено в  true , Aspose.Words использует встроенные данные EMF при рендеринге.

Когда это значение установлено в  false , Aspose.Words использует данные WMF при рендеринге.

Эта опция используется только когда метафайл рендерится как векторная графика. Когда метафайл рендерится в bitmap, данные WMF всегда используются.

Значение по умолчанию —  true .

 **Examples:** 

Показывает, как настроить параметры рендеринга, связанные с Enhanced Windows Metafile, при сохранении в PDF.

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
boolean - Значение, определяющее, как должны рендериться WMF‑метафайлы с вложенными EMF‑метафайлами.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


Получает значение, определяющее, следует ли использовать GDI+ для эмуляции растровых операций.

 **Remarks:** 

Библиотека Windows GDI+ может использоваться для эмуляции растровых операций. Она предоставляет поддержку всех растровых операций по сравнению с собственной эмуляцией Aspose.Words, но в некоторых случаях производительность может быть ниже.

Когда это значение установлено в  true , Aspose.Words использует GDI+ для эмуляции растровых операций.

Когда это значение установлено в  false , Aspose.Words использует собственную реализацию эмуляции растровых операций.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию — false.

 **Examples:** 

Показывает, как установить режим рендеринга при сохранении документов с изображениями Windows Metafile в другие форматы изображений.

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
boolean — Значение, определяющее, использовать ли GDI+ для эмуляции растровых операций.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


Устанавливает значение, определяющее, как должны рендериться EMF+ Dual метафайлы.

 **Remarks:** 

EMF+ Dual метафайлы содержат как части EMF+, так и части EMF. MS Word и GDI+ всегда рендерят часть EMF+. Aspose.Words в настоящее время не полностью поддерживает все записи EMF+ и в некоторых случаях результат рендеринга части EMF выглядит лучше, чем результат рендеринга части EMF+.

Этот параметр используется только когда метафайл рендерится как векторная графика. Когда метафайл рендерится в bitmap, часть EMF+ всегда используется.

Значение по умолчанию — [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

 **Examples:** 

Показывает, как настроить параметры рендеринга, связанные с Enhanced Windows Metafile, при сохранении в PDF.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее, как должны отображаться метафайлы EMF+ Dual. Значение должно быть одной из констант [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/). |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


Устанавливает значение, определяющее, следует ли эмулировать растровые операции.

 **Remarks:** 

В метафайлах могут использоваться специфические растровые операции. Их нельзя отобразить напрямую в векторную графику. Эмуляция растровых операций требует частичной растеризации полученной векторной графики, что может повлиять на производительность рендеринга метафайла.

Когда это значение установлено в  true , Aspose.Words эмулирует растровые операции. Полученный вывод может быть частично растеризован, и производительность может быть ниже.

Когда это значение установлено в  false , Aspose.Words не эмулирует растровые операции. Когда Aspose.Words встречает растровую операцию в метафайле, он переходит к рендерингу метафайла в bitmap, используя операционную систему.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию —  true .

 **Examples:** 

Показывает, что добавлен резервный режим рендеринга в bitmap и изменён тип предупреждений о неподдерживаемых записях метафайла.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, определяющее, следует ли эмулировать растровые операции. |

### setEmulateRenderingToSizeOnPage(boolean value) {#setEmulateRenderingToSizeOnPage-boolean}
```
public void setEmulateRenderingToSizeOnPage(boolean value)
```


Устанавливает значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию.

 **Remarks:** 

Когда метафайлы отображаются в MS Word, некоторые графические элементы могут масштабироваться в соответствии с фактическим размером метафайла в пикселях. То есть даже масштабирование может влиять на отображение метафайла.

Когда это значение установлено в  true , Aspose.Words эмулирует рендеринг в соответствии с размером метафайла на странице. Размер в пикселях рассчитывается из размера метафайла на странице и указанного [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Когда это значение установлено в  false , Aspose.Words эмулирует рендеринг метафайла до его стандартного размера в пикселях.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию —  true .

 **Examples:** 

Показывает, как отображать метафайл в соответствии с размером на странице.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию. |

### setEmulateRenderingToSizeOnPageResolution(int value) {#setEmulateRenderingToSizeOnPageResolution-int}
```
public void setEmulateRenderingToSizeOnPageResolution(int value)
```


Устанавливает разрешение в пикселях на дюйм для эмуляции рендеринга метафайла к размеру на странице.

 **Remarks:** 

Эта опция используется только когда [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) установлен в  true .

Значение по умолчанию — 96. Это стандартное разрешение отображения. То есть рендеринг метафайла будет эмулировать отображение метафайла в MS Word с коэффициентом масштабирования 100%.

 **Examples:** 

Показывает, как отображать метафайл в соответствии с размером на странице.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Разрешение в пикселях на дюйм для эмуляции рендеринга метафайла к размеру на странице. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


Устанавливает значение, определяющее, как должны рендериться изображения метафайлов.

 **Remarks:** 

Значение по умолчанию зависит от формата сохранения. Для изображений это [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Для других форматов это [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Показывает, что добавлен резервный режим рендеринга в bitmap и изменён тип предупреждений о неподдерживаемых записях метафайла.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее, как должны отображаться изображения метафайлов. Значение должно быть одной из констант [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/). |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Устанавливает значение, определяющее, как должны рендериться WMF метафайлы с вложенными EMF метафайлами.

 **Remarks:** 

WMF‑метафайлы могут содержать встроенные данные EMF. В большинстве случаев MS Word использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда это значение установлено в  true , Aspose.Words использует встроенные данные EMF при рендеринге.

Когда это значение установлено в  false , Aspose.Words использует данные WMF при рендеринге.

Эта опция используется только когда метафайл рендерится как векторная графика. Когда метафайл рендерится в bitmap, данные WMF всегда используются.

Значение по умолчанию —  true .

 **Examples:** 

Показывает, как настроить параметры рендеринга, связанные с Enhanced Windows Metafile, при сохранении в PDF.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, определяющее, как должны отображаться WMF‑метафайлы с вложенными EMF‑метафайлами. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


Устанавливает значение, определяющее, следует ли использовать GDI+ для эмуляции растровых операций.

 **Remarks:** 

Библиотека Windows GDI+ может использоваться для эмуляции растровых операций. Она предоставляет поддержку всех растровых операций по сравнению с собственной эмуляцией Aspose.Words, но в некоторых случаях производительность может быть ниже.

Когда это значение установлено в  true , Aspose.Words использует GDI+ для эмуляции растровых операций.

Когда это значение установлено в  false , Aspose.Words использует собственную реализацию эмуляции растровых операций.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию — false.

 **Examples:** 

Показывает, как установить режим рендеринга при сохранении документов с изображениями Windows Metafile в другие форматы изображений.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, определяющее, использовать ли GDI+ для эмуляции растровых операций. |

