---
title: "MetafileRenderingOptions"
linktitle: "MetafileRenderingOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Angeben zusätzlicher Metafile-Renderoptionen in Java."
type: docs
weight: 468
url: /de/java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Ermöglicht die Angabe zusätzlicher Renderoptionen für Metadateien.

Um mehr zu erfahren, besuchen Sie den [ Handling Windows Metafiles ][Handling Windows Metafiles] Dokumentationsartikel.

 **Examples:** 

Zeigt, dass ein Fallback zur Bitmap-Renderung hinzugefügt wurde und der Typ von Warnungen über nicht unterstützte Metadatei-Einträge geändert wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | Gibt einen Wert zurück, der bestimmt, wie EMF+ Dual-Metafiles gerendert werden sollen. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | Gibt einen Wert zurück, der bestimmt, ob die Rasteroperationen emuliert werden sollen. |
| [getEmulateRenderingToSizeOnPage()](#getEmulateRenderingToSizeOnPage) | Gibt einen Wert zurück, der bestimmt, ob das Metafile-Rendering die Anzeige des Metafiles gemäß der Größe auf der Seite oder in seiner Standardgröße emuliert. |
| [getEmulateRenderingToSizeOnPageResolution()](#getEmulateRenderingToSizeOnPageResolution) | Gibt die Auflösung in Pixel pro Zoll für die Emulation des Metafile-Renderings zur Größe auf der Seite zurück. |
| [getRenderingMode()](#getRenderingMode) | Gibt einen Wert zurück, der bestimmt, wie Metafile-Bilder gerendert werden sollen. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | Gibt einen Wert zurück, der bestimmt, wie WMF-Metafiles mit eingebetteten EMF-Metafiles gerendert werden sollen. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | Ermittelt einen Wert, der festlegt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll oder nicht. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | Legt einen Wert fest, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | Legt einen Wert fest, der bestimmt, ob Rasteroperationen emuliert werden sollen oder nicht. |
| [setEmulateRenderingToSizeOnPage(boolean value)](#setEmulateRenderingToSizeOnPage-boolean) | Legt einen Wert fest, der bestimmt, ob die Metadatei-Darstellung die Anzeige der Metadatei gemäß der Größe auf der Seite emuliert oder die Anzeige der Metadatei in ihrer Standardgröße. |
| [setEmulateRenderingToSizeOnPageResolution(int value)](#setEmulateRenderingToSizeOnPageResolution-int) | Legt die Auflösung in Pixel pro Zoll für die Emulation der Metadatei-Darstellung auf die Größe auf der Seite fest. |
| [setRenderingMode(int value)](#setRenderingMode-int) | Legt einen Wert fest, der bestimmt, wie Metadatei-Bilder gerendert werden sollen. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | Legt einen Wert fest, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | Legt einen Wert fest, der bestimmt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll oder nicht. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


Gibt einen Wert zurück, der bestimmt, wie EMF+ Dual-Metafiles gerendert werden sollen.

 **Remarks:** 

EMF+ Dual-Metadateien enthalten sowohl EMF+- als auch EMF-Teile. MS Word und GDI+ rendern immer den EMF+-Teil. Aspose.Words unterstützt derzeit nicht alle EMF+-Datensätze vollständig, und in einigen Fällen sieht das Rendering-Ergebnis des EMF-Teils besser aus als das Rendering-Ergebnis des EMF+-Teils.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wird die Metadatei in ein Bitmap gerendert, wird stets der EMF+-Teil verwendet.

Der Standardwert ist [EmfPlusDualRenderingMode.EMF\\_PLUS\\_WITH\\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\\#EMF-PLUS-WITH-FALLBACK).

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

**Returns:**
int – Ein Wert, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen. Der zurückgegebene Wert ist einer der Konstanten von [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/).
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


Gibt einen Wert zurück, der bestimmt, ob die Rasteroperationen emuliert werden sollen.

 **Remarks:** 

Spezifische Rasteroperationen können in Metadateien verwendet werden. Sie können nicht direkt in Vektorgrafiken gerendert werden. Die Emulation von Rasteroperationen erfordert eine teilweise Rasterung der resultierenden Vektorgrafiken, was die Rendering‑Leistung der Metadatei beeinträchtigen kann.

Wenn dieser Wert auf true gesetzt ist, emuliert Aspose.Words die Rasteroperationen. Die resultierende Ausgabe kann teilweise gerastert sein und die Leistung könnte langsamer sein.

Wenn dieser Wert auf false gesetzt ist, emuliert Aspose.Words die Rasteroperationen nicht. Wenn Aspose.Words in einer Metadatei eine Rasteroperation erkennt, greift es auf die Rendering‑Methode zurück, bei der die Metadatei mithilfe des Betriebssystems in ein Bitmap gerendert wird.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist  true .

 **Examples:** 

Zeigt, dass ein Fallback zur Bitmap-Renderung hinzugefügt wurde und der Typ von Warnungen über nicht unterstützte Metadatei-Einträge geändert wird.

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
boolean – Ein Wert, der bestimmt, ob Rasteroperationen emuliert werden sollen oder nicht.
### getEmulateRenderingToSizeOnPage() {#getEmulateRenderingToSizeOnPage}
```
public boolean getEmulateRenderingToSizeOnPage()
```


Gibt einen Wert zurück, der bestimmt, ob das Metafile-Rendering die Anzeige des Metafiles gemäß der Größe auf der Seite oder in seiner Standardgröße emuliert.

 **Remarks:** 

Wenn Metadateien in MS Word angezeigt werden, können einige Grafiken gemäß der tatsächlichen Metadateigröße in Pixeln skaliert werden. Das heißt, selbst das Zoomen kann die Anzeige der Metadatei beeinflussen.

Wenn dieser Wert auf true gesetzt ist, emuliert Aspose.Words das Rendering gemäß der Metadateigröße auf der Seite. Die Größe in Pixeln wird aus der Metadateigröße auf der Seite und der angegebenen [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\\#setEmulateRenderingToSizeOnPageResolution-int) berechnet.

Wenn dieser Wert auf false gesetzt ist, emuliert Aspose.Words die Metadatei-Darstellung in ihrer Standardgröße in Pixeln.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie die Anzeige der Metadatei gemäß der Größe auf der Seite erfolgt.

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
boolean – Ein Wert, der bestimmt, ob die Metadatei-Darstellung die Anzeige der Metadatei gemäß der Größe auf der Seite oder die Anzeige der Metadatei in ihrer Standardgröße emuliert.
### getEmulateRenderingToSizeOnPageResolution() {#getEmulateRenderingToSizeOnPageResolution}
```
public int getEmulateRenderingToSizeOnPageResolution()
```


Gibt die Auflösung in Pixel pro Zoll für die Emulation des Metafile-Renderings zur Größe auf der Seite zurück.

 **Remarks:** 

Diese Option wird nur verwendet, wenn [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) auf true gesetzt ist.

Der Standardwert ist 96. Dies ist eine Standardanzeigeauflösung. D.h. die Metadatei-Darstellung emuliert die Anzeige der Metadatei in MS Word mit einem Zoomfaktor von 100 %.

 **Examples:** 

Zeigt, wie die Anzeige der Metadatei gemäß der Größe auf der Seite erfolgt.

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
int – Die Auflösung in Pixeln pro Zoll für die Emulation der Metadatei-Darstellung zur Größe auf der Seite.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


Gibt einen Wert zurück, der bestimmt, wie Metafile-Bilder gerendert werden sollen.

 **Remarks:** 

Der Standardwert hängt vom Speicherformat ab. Für Bilder ist er [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Für andere Formate ist er [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Zeigt, dass ein Fallback zur Bitmap-Renderung hinzugefügt wurde und der Typ von Warnungen über nicht unterstützte Metadatei-Einträge geändert wird.

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
int – Ein Wert, der bestimmt, wie Metadatei-Bilder gerendert werden sollen. Der zurückgegebene Wert ist einer der Konstanten von [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/).
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


Gibt einen Wert zurück, der bestimmt, wie WMF-Metafiles mit eingebetteten EMF-Metafiles gerendert werden sollen.

 **Remarks:** 

WMF-Metadateien können eingebettete EMF-Daten enthalten. MS Word verwendet in den meisten Fällen eingebettete EMF-Daten. GDI+ verwendet immer WMF-Daten.

Wenn dieser Wert auf true gesetzt ist, verwendet Aspose.Words beim Rendern eingebettete EMF-Daten.

Wenn dieser Wert auf false gesetzt ist, verwendet Aspose.Words beim Rendern WMF-Daten.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wenn die Metadatei in ein Bitmap gerendert wird, werden immer WMF-Daten verwendet.

Der Standardwert ist  true .

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

**Returns:**
boolean – Ein Wert, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


Ermittelt einen Wert, der festlegt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll oder nicht.

 **Remarks:** 

Die Windows GDI+-Bibliothek könnte verwendet werden, um Rasteroperationen zu emulieren. Sie bietet im Vergleich zur eigenen Emulation von Aspose.Words Unterstützung für alle Rasteroperationen, jedoch kann die Leistung in einigen Fällen langsamer sein.

Wenn dieser Wert auf true gesetzt ist, verwendet Aspose.Words GDI+ für die Emulation von Rasteroperationen.

Wenn dieser Wert auf false gesetzt ist, verwendet Aspose.Words seine eigene Implementierung der Emulation von Rasteroperationen.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie der Rendermodus beim Speichern von Dokumenten mit Windows-Metadatei-Bildern in andere Bildformate festgelegt wird.

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
boolean – Ein Wert, der bestimmt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll oder nicht.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


Legt einen Wert fest, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen.

 **Remarks:** 

EMF+ Dual-Metadateien enthalten sowohl EMF+- als auch EMF-Teile. MS Word und GDI+ rendern immer den EMF+-Teil. Aspose.Words unterstützt derzeit nicht alle EMF+-Datensätze vollständig, und in einigen Fällen sieht das Rendering-Ergebnis des EMF-Teils besser aus als das Rendering-Ergebnis des EMF+-Teils.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wird die Metadatei in ein Bitmap gerendert, wird stets der EMF+-Teil verwendet.

Der Standardwert ist [EmfPlusDualRenderingMode.EMF\\_PLUS\\_WITH\\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\\#EMF-PLUS-WITH-FALLBACK).

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein Wert, der bestimmt, wie EMF+ Dual-Metadateien gerendert werden sollen. Der Wert muss einer der Konstanten von [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/) sein. |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


Legt einen Wert fest, der bestimmt, ob Rasteroperationen emuliert werden sollen oder nicht.

 **Remarks:** 

Spezifische Rasteroperationen können in Metadateien verwendet werden. Sie können nicht direkt in Vektorgrafiken gerendert werden. Die Emulation von Rasteroperationen erfordert eine teilweise Rasterung der resultierenden Vektorgrafiken, was die Rendering‑Leistung der Metadatei beeinträchtigen kann.

Wenn dieser Wert auf true gesetzt ist, emuliert Aspose.Words die Rasteroperationen. Die resultierende Ausgabe kann teilweise gerastert sein und die Leistung könnte langsamer sein.

Wenn dieser Wert auf false gesetzt ist, emuliert Aspose.Words die Rasteroperationen nicht. Wenn Aspose.Words in einer Metadatei eine Rasteroperation erkennt, greift es auf die Rendering‑Methode zurück, bei der die Metadatei mithilfe des Betriebssystems in ein Bitmap gerendert wird.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist  true .

 **Examples:** 

Zeigt, dass ein Fallback zur Bitmap-Renderung hinzugefügt wurde und der Typ von Warnungen über nicht unterstützte Metadatei-Einträge geändert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der bestimmt, ob Rasteroperationen emuliert werden sollen oder nicht. |

### setEmulateRenderingToSizeOnPage(boolean value) {#setEmulateRenderingToSizeOnPage-boolean}
```
public void setEmulateRenderingToSizeOnPage(boolean value)
```


Legt einen Wert fest, der bestimmt, ob die Metadatei-Darstellung die Anzeige der Metadatei gemäß der Größe auf der Seite emuliert oder die Anzeige der Metadatei in ihrer Standardgröße.

 **Remarks:** 

Wenn Metadateien in MS Word angezeigt werden, können einige Grafiken gemäß der tatsächlichen Metadateigröße in Pixeln skaliert werden. Das heißt, selbst das Zoomen kann die Anzeige der Metadatei beeinflussen.

Wenn dieser Wert auf true gesetzt ist, emuliert Aspose.Words das Rendering gemäß der Metadateigröße auf der Seite. Die Größe in Pixeln wird aus der Metadateigröße auf der Seite und der angegebenen [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\\#setEmulateRenderingToSizeOnPageResolution-int) berechnet.

Wenn dieser Wert auf false gesetzt ist, emuliert Aspose.Words die Metadatei-Darstellung in ihrer Standardgröße in Pixeln.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie die Anzeige der Metadatei gemäß der Größe auf der Seite erfolgt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der bestimmt, ob die Metadatei-Darstellung die Anzeige der Metadatei gemäß der Größe auf der Seite oder die Anzeige der Metadatei in ihrer Standardgröße emuliert. |

### setEmulateRenderingToSizeOnPageResolution(int value) {#setEmulateRenderingToSizeOnPageResolution-int}
```
public void setEmulateRenderingToSizeOnPageResolution(int value)
```


Legt die Auflösung in Pixel pro Zoll für die Emulation der Metadatei-Darstellung auf die Größe auf der Seite fest.

 **Remarks:** 

Diese Option wird nur verwendet, wenn [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) auf true gesetzt ist.

Der Standardwert ist 96. Dies ist eine Standardanzeigeauflösung. D.h. die Metadatei-Darstellung emuliert die Anzeige der Metadatei in MS Word mit einem Zoomfaktor von 100 %.

 **Examples:** 

Zeigt, wie die Anzeige der Metadatei gemäß der Größe auf der Seite erfolgt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Auflösung in Pixeln pro Zoll für die Emulation der Metadatei-Darstellung zur Größe auf der Seite. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


Legt einen Wert fest, der bestimmt, wie Metadatei-Bilder gerendert werden sollen.

 **Remarks:** 

Der Standardwert hängt vom Speicherformat ab. Für Bilder ist er [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Für andere Formate ist er [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Zeigt, dass ein Fallback zur Bitmap-Renderung hinzugefügt wurde und der Typ von Warnungen über nicht unterstützte Metadatei-Einträge geändert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein Wert, der bestimmt, wie Metadatei‑Bilder gerendert werden sollen. Der Wert muss einer der Konstanten von [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/) sein. |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Legt einen Wert fest, der bestimmt, wie WMF-Metadateien mit eingebetteten EMF-Metadateien gerendert werden sollen.

 **Remarks:** 

WMF-Metadateien können eingebettete EMF-Daten enthalten. MS Word verwendet in den meisten Fällen eingebettete EMF-Daten. GDI+ verwendet immer WMF-Daten.

Wenn dieser Wert auf true gesetzt ist, verwendet Aspose.Words beim Rendern eingebettete EMF-Daten.

Wenn dieser Wert auf false gesetzt ist, verwendet Aspose.Words beim Rendern WMF-Daten.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird. Wenn die Metadatei in ein Bitmap gerendert wird, werden immer WMF-Daten verwendet.

Der Standardwert ist  true .

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der bestimmt, wie WMF‑Metadateien mit eingebetteten EMF‑Metadateien gerendert werden sollen. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


Legt einen Wert fest, der bestimmt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll oder nicht.

 **Remarks:** 

Die Windows GDI+-Bibliothek könnte verwendet werden, um Rasteroperationen zu emulieren. Sie bietet im Vergleich zur eigenen Emulation von Aspose.Words Unterstützung für alle Rasteroperationen, jedoch kann die Leistung in einigen Fällen langsamer sein.

Wenn dieser Wert auf true gesetzt ist, verwendet Aspose.Words GDI+ für die Emulation von Rasteroperationen.

Wenn dieser Wert auf false gesetzt ist, verwendet Aspose.Words seine eigene Implementierung der Emulation von Rasteroperationen.

Diese Option wird nur verwendet, wenn die Metadatei als Vektorgrafik gerendert wird.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie der Rendermodus beim Speichern von Dokumenten mit Windows-Metadatei-Bildern in andere Bildformate festgelegt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der festlegt, ob GDI+ für die Emulation von Rasteroperationen verwendet werden soll oder nicht. |

