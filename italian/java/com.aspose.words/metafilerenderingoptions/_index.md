---
title: "MetafileRenderingOptions"
linktitle: "MetafileRenderingOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare opzioni aggiuntive di rendering dei metafile in Java."
type: docs
weight: 468
url: /it/java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Consente di specificare opzioni aggiuntive di rendering dei metafili.

Per saperne di più, visita l'articolo di documentazione [ Handling Windows Metafiles ][Handling Windows Metafiles].

 **Examples:** 

Mostra aggiunto un fallback al rendering bitmap e modifica il tipo di avvisi sui record metafile non supportati.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | Ottiene un valore che determina come devono essere renderizzati i metafile EMF+ Dual. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | Ottiene un valore che determina se le operazioni raster devono essere emulate o meno. |
| [getEmulateRenderingToSizeOnPage()](#getEmulateRenderingToSizeOnPage) | Ottiene un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita. |
| [getEmulateRenderingToSizeOnPageResolution()](#getEmulateRenderingToSizeOnPageResolution) | Ottiene la risoluzione in pixel per pollice per l'emulazione del rendering del metafile alle dimensioni sulla pagina. |
| [getRenderingMode()](#getRenderingMode) | Ottiene un valore che determina come devono essere renderizzate le immagini del metafile. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | Ottiene un valore che determina come devono essere renderizzati i metafile WMF con metafile EMF incorporati. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | Ottiene un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | Imposta un valore che determina come devono essere renderizzati i metafile EMF+ Dual. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | Imposta un valore che determina se le operazioni raster devono essere emulate o meno. |
| [setEmulateRenderingToSizeOnPage(boolean value)](#setEmulateRenderingToSizeOnPage-boolean) | Imposta un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita. |
| [setEmulateRenderingToSizeOnPageResolution(int value)](#setEmulateRenderingToSizeOnPageResolution-int) | Imposta la risoluzione in pixel per pollice per l'emulazione del rendering del metafile alle dimensioni sulla pagina. |
| [setRenderingMode(int value)](#setRenderingMode-int) | Imposta un valore che determina come devono essere renderizzate le immagini del metafile. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | Imposta un valore che determina come devono essere renderizzati i metafile WMF con metafile EMF incorporati. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | Imposta un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


Ottiene un valore che determina come devono essere renderizzati i metafile EMF+ Dual.

 **Remarks:** 

I metafile EMF+ Dual contengono sia parti EMF+ che EMF. MS Word e GDI+ rendono sempre la parte EMF+. Aspose.Words attualmente non supporta completamente tutti i record EMF+ e in alcuni casi il risultato del rendering della parte EMF sembra migliore rispetto al risultato del rendering della parte EMF+.

Questa opzione è utilizzata solo quando il metafile viene renderizzato come grafica vettoriale. Quando il metafile viene renderizzato in bitmap, la parte EMF+ è sempre utilizzata.

Il valore predefinito è [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

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

**Returns:**
int - Un valore che determina come devono essere renderizzati i metafili EMF+ Dual. Il valore restituito è una delle costanti di [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/).
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


Ottiene un valore che determina se le operazioni raster devono essere emulate o meno.

 **Remarks:** 

Operazioni raster specifiche potrebbero essere utilizzate nei metafili. Non possono essere renderizzate direttamente in grafica vettoriale. L'emulazione delle operazioni raster richiede una rasterizzazione parziale della grafica vettoriale risultante, il che può influire sulle prestazioni del rendering del metafile.

Quando questo valore è impostato su true, Aspose.Words emula le operazioni raster. L'output risultante potrebbe essere parzialmente rasterizzato e le prestazioni potrebbero essere più lente.

Quando questo valore è impostato su false, Aspose.Words non emula le operazioni raster. Quando Aspose.Words incontra un'operazione raster in un metafile, ricade nel rendering del metafile in una bitmap utilizzando il sistema operativo.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale.

Il valore predefinito è  true .

 **Examples:** 

Mostra aggiunto un fallback al rendering bitmap e modifica il tipo di avvisi sui record metafile non supportati.

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
boolean - Un valore che determina se le operazioni raster debbano o meno essere emulate.
### getEmulateRenderingToSizeOnPage() {#getEmulateRenderingToSizeOnPage}
```
public boolean getEmulateRenderingToSizeOnPage()
```


Ottiene un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita.

 **Remarks:** 

Quando i metafili vengono visualizzati in MS Word, alcune grafiche possono essere scalate in base alle dimensioni effettive del metafile in pixel. Cioè, anche lo zoom può influire sulla visualizzazione del metafile.

Quando questo valore è impostato su true, Aspose.Words emula il rendering in base alle dimensioni del metafile sulla pagina. Le dimensioni in pixel sono calcolate dalle dimensioni del metafile sulla pagina e dai metodi specificati [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Quando questo valore è impostato su false, Aspose.Words emula il rendering del metafile nella sua dimensione predefinita in pixel.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale.

Il valore predefinito è  true .

 **Examples:** 

Mostra come visualizzare il metafile in base alle dimensioni sulla pagina.

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
boolean - Un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita.
### getEmulateRenderingToSizeOnPageResolution() {#getEmulateRenderingToSizeOnPageResolution}
```
public int getEmulateRenderingToSizeOnPageResolution()
```


Ottiene la risoluzione in pixel per pollice per l'emulazione del rendering del metafile alle dimensioni sulla pagina.

 **Remarks:** 

Questa opzione è utilizzata solo quando [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) è impostata su true.

Il valore predefinito è 96. Questa è una risoluzione di visualizzazione predefinita. Cioè, il rendering del metafile emulerà la visualizzazione del metafile in MS Word con un fattore di zoom del 100%.

 **Examples:** 

Mostra come visualizzare il metafile in base alle dimensioni sulla pagina.

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
int - La risoluzione in pixel per pollice per l'emulazione del rendering del metafile alle dimensioni sulla pagina.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


Ottiene un valore che determina come devono essere renderizzate le immagini del metafile.

 **Remarks:** 

Il valore predefinito dipende dal formato di salvataggio. Per le immagini è [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Per gli altri formati è [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Mostra aggiunto un fallback al rendering bitmap e modifica il tipo di avvisi sui record metafile non supportati.

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
int - Un valore che determina come devono essere renderizzate le immagini dei metafili. Il valore restituito è una delle costanti di [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/).
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


Ottiene un valore che determina come devono essere renderizzati i metafile WMF con metafile EMF incorporati.

 **Remarks:** 

I metafili WMF potrebbero contenere dati EMF incorporati. MS Word nella maggior parte dei casi utilizza dati EMF incorporati. GDI+ utilizza sempre dati WMF.

Quando questo valore è impostato su true, Aspose.Words utilizza dati EMF incorporati durante il rendering.

Quando questo valore è impostato su false, Aspose.Words utilizza dati WMF durante il rendering.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale. Quando il metafile è renderizzato in bitmap, i dati WMF sono sempre utilizzati.

Il valore predefinito è  true .

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

**Returns:**
boolean - Un valore che determina come devono essere renderizzati i metafili WMF con metafili EMF incorporati.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


Ottiene un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster.

 **Remarks:** 

La libreria Windows GDI+ potrebbe essere utilizzata per emulare le operazioni raster. Fornisce supporto per tutte le operazioni raster rispetto all'emulazione propria di Aspose.Words, ma le prestazioni potrebbero essere più lente in alcuni casi.

Quando questo valore è impostato su true, Aspose.Words utilizza GDI+ per l'emulazione delle operazioni raster.

Quando questo valore è impostato su false, Aspose.Words utilizza la propria implementazione dell'emulazione delle operazioni raster.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale.

Il valore predefinito è  false .

 **Examples:** 

Mostra come impostare la modalità di rendering quando si salvano documenti con immagini Windows Metafile in altri formati immagine.

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
boolean - Un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


Imposta un valore che determina come devono essere renderizzati i metafile EMF+ Dual.

 **Remarks:** 

I metafile EMF+ Dual contengono sia parti EMF+ che EMF. MS Word e GDI+ rendono sempre la parte EMF+. Aspose.Words attualmente non supporta completamente tutti i record EMF+ e in alcuni casi il risultato del rendering della parte EMF sembra migliore rispetto al risultato del rendering della parte EMF+.

Questa opzione è utilizzata solo quando il metafile viene renderizzato come grafica vettoriale. Quando il metafile viene renderizzato in bitmap, la parte EMF+ è sempre utilizzata.

Il valore predefinito è [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Un valore che determina come devono essere renderizzati i metafili EMF+ Dual. Il valore deve essere uno dei costanti [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/). |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


Imposta un valore che determina se le operazioni raster devono essere emulate o meno.

 **Remarks:** 

Operazioni raster specifiche potrebbero essere utilizzate nei metafili. Non possono essere renderizzate direttamente in grafica vettoriale. L'emulazione delle operazioni raster richiede una rasterizzazione parziale della grafica vettoriale risultante, il che può influire sulle prestazioni del rendering del metafile.

Quando questo valore è impostato su true, Aspose.Words emula le operazioni raster. L'output risultante potrebbe essere parzialmente rasterizzato e le prestazioni potrebbero essere più lente.

Quando questo valore è impostato su false, Aspose.Words non emula le operazioni raster. Quando Aspose.Words incontra un'operazione raster in un metafile, ricade nel rendering del metafile in una bitmap utilizzando il sistema operativo.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale.

Il valore predefinito è  true .

 **Examples:** 

Mostra aggiunto un fallback al rendering bitmap e modifica il tipo di avvisi sui record metafile non supportati.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che determina se le operazioni raster debbano essere emulate o meno. |

### setEmulateRenderingToSizeOnPage(boolean value) {#setEmulateRenderingToSizeOnPage-boolean}
```
public void setEmulateRenderingToSizeOnPage(boolean value)
```


Imposta un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita.

 **Remarks:** 

Quando i metafili vengono visualizzati in MS Word, alcune grafiche possono essere scalate in base alle dimensioni effettive del metafile in pixel. Cioè, anche lo zoom può influire sulla visualizzazione del metafile.

Quando questo valore è impostato su true, Aspose.Words emula il rendering in base alle dimensioni del metafile sulla pagina. Le dimensioni in pixel sono calcolate dalle dimensioni del metafile sulla pagina e dai metodi specificati [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Quando questo valore è impostato su false, Aspose.Words emula il rendering del metafile nella sua dimensione predefinita in pixel.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale.

Il valore predefinito è  true .

 **Examples:** 

Mostra come visualizzare il metafile in base alle dimensioni sulla pagina.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita. |

### setEmulateRenderingToSizeOnPageResolution(int value) {#setEmulateRenderingToSizeOnPageResolution-int}
```
public void setEmulateRenderingToSizeOnPageResolution(int value)
```


Imposta la risoluzione in pixel per pollice per l'emulazione del rendering del metafile alle dimensioni sulla pagina.

 **Remarks:** 

Questa opzione è utilizzata solo quando [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) è impostata su true.

Il valore predefinito è 96. Questa è una risoluzione di visualizzazione predefinita. Cioè, il rendering del metafile emulerà la visualizzazione del metafile in MS Word con un fattore di zoom del 100%.

 **Examples:** 

Mostra come visualizzare il metafile in base alle dimensioni sulla pagina.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La risoluzione in pixel per pollice per l'emulazione del rendering del metafile alle dimensioni sulla pagina. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


Imposta un valore che determina come devono essere renderizzate le immagini del metafile.

 **Remarks:** 

Il valore predefinito dipende dal formato di salvataggio. Per le immagini è [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Per gli altri formati è [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Mostra aggiunto un fallback al rendering bitmap e modifica il tipo di avvisi sui record metafile non supportati.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Un valore che determina come devono essere renderizzate le immagini metafile. Il valore deve essere uno dei costanti [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/). |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Imposta un valore che determina come devono essere renderizzati i metafile WMF con metafile EMF incorporati.

 **Remarks:** 

I metafili WMF potrebbero contenere dati EMF incorporati. MS Word nella maggior parte dei casi utilizza dati EMF incorporati. GDI+ utilizza sempre dati WMF.

Quando questo valore è impostato su true, Aspose.Words utilizza dati EMF incorporati durante il rendering.

Quando questo valore è impostato su false, Aspose.Words utilizza dati WMF durante il rendering.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale. Quando il metafile è renderizzato in bitmap, i dati WMF sono sempre utilizzati.

Il valore predefinito è  true .

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che determina come devono essere renderizzati i metafili WMF con metafili EMF incorporati. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


Imposta un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster.

 **Remarks:** 

La libreria Windows GDI+ potrebbe essere utilizzata per emulare le operazioni raster. Fornisce supporto per tutte le operazioni raster rispetto all'emulazione propria di Aspose.Words, ma le prestazioni potrebbero essere più lente in alcuni casi.

Quando questo valore è impostato su true, Aspose.Words utilizza GDI+ per l'emulazione delle operazioni raster.

Quando questo valore è impostato su false, Aspose.Words utilizza la propria implementazione dell'emulazione delle operazioni raster.

Questa opzione è utilizzata solo quando il metafile è renderizzato come grafica vettoriale.

Il valore predefinito è  false .

 **Examples:** 

Mostra come impostare la modalità di rendering quando si salvano documenti con immagini Windows Metafile in altri formati immagine.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster. |

