---
title: "MetafileRenderingOptions"
linktitle: "MetafileRenderingOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar opciones adicionales de renderizado de metaficheros en Java."
type: docs
weight: 468
url: /es/java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Permite especificar opciones adicionales de renderizado de metaficheros.

Para obtener más información, visite el artículo de documentación [ Manejo de Metaficheros de Windows ][Handling Windows Metafiles].

 **Examples:** 

Muestra una alternativa añadida a la renderización de mapa de bits y cambia el tipo de advertencias sobre registros de metarchivo no compatibles.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | Obtiene un valor que determina cómo se deben renderizar los metaficheros EMF+ Dual. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | Obtiene un valor que determina si se deben emular o no las operaciones raster. |
| [getEmulateRenderingToSizeOnPage()](#getEmulateRenderingToSizeOnPage) | Obtiene un valor que determina si el renderizado del metafichero emula la visualización del metafichero según el tamaño en la página o la visualización del metafichero en su tamaño predeterminado. |
| [getEmulateRenderingToSizeOnPageResolution()](#getEmulateRenderingToSizeOnPageResolution) | Obtiene la resolución en píxeles por pulgada para la emulación del renderizado del metafichero al tamaño en la página. |
| [getRenderingMode()](#getRenderingMode) | Obtiene un valor que determina cómo se deben renderizar las imágenes del metafichero. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | Obtiene un valor que determina cómo se deben renderizar los metaficheros WMF con metaficheros EMF incrustados. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | Obtiene un valor que determina si se debe usar GDI+ para la emulación de operaciones raster o no. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | Establece un valor que determina cómo se deben renderizar los metaficheros EMF+ Dual. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | Establece un valor que determina si se deben emular o no las operaciones raster. |
| [setEmulateRenderingToSizeOnPage(boolean value)](#setEmulateRenderingToSizeOnPage-boolean) | Establece un valor que determina si el renderizado del metafichero emula la visualización del metafichero según el tamaño en la página o la visualización del metafichero en su tamaño predeterminado. |
| [setEmulateRenderingToSizeOnPageResolution(int value)](#setEmulateRenderingToSizeOnPageResolution-int) | Establece la resolución en píxeles por pulgada para la emulación del renderizado del metafichero al tamaño en la página. |
| [setRenderingMode(int value)](#setRenderingMode-int) | Establece un valor que determina cómo se deben renderizar las imágenes del metafichero. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | Establece un valor que determina cómo se deben renderizar los metaficheros WMF con metaficheros EMF incrustados. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | Establece un valor que determina si se debe usar GDI+ para la emulación de operaciones raster o no. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


Obtiene un valor que determina cómo se deben renderizar los metaficheros EMF+ Dual.

 **Remarks:** 

Los metaficheros EMF+ Dual contienen tanto partes EMF+ como EMF. MS Word y GDI+ siempre renderizan la parte EMF+. Aspose.Words actualmente no soporta completamente todos los registros EMF+ y, en algunos casos, el resultado del renderizado de la parte EMF se ve mejor que el resultado del renderizado de la parte EMF+.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales. Cuando el metafichero se renderiza a bitmap, siempre se usa la parte EMF+.

El valor predeterminado es [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

 **Examples:** 

Muestra cómo configurar las opciones de renderizado relacionadas con Enhanced Windows Metafile al guardar en PDF.

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
int - Un valor que determina cómo deben renderizarse los metaficheros EMF+ Dual. El valor devuelto es una de las constantes de [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/).
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


Obtiene un valor que determina si se deben emular o no las operaciones raster.

 **Remarks:** 

Se pueden usar operaciones raster específicas en los metaficheros. No pueden renderizarse directamente a gráficos vectoriales. Emular operaciones raster requiere una rasterización parcial de los gráficos vectoriales resultantes, lo que puede afectar el rendimiento de renderizado del metafichero.

Cuando este valor se establece en  true , **Aspose.Words** emula las operaciones raster. La salida resultante puede estar parcialmente rasterizada y el rendimiento podría ser más lento.

Cuando este valor se establece en  false , **Aspose.Words** no emula las operaciones raster. Cuando **Aspose.Words** encuentra una operación raster en un metafichero, recurre a renderizar el metafichero en un mapa de bits utilizando el sistema operativo.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es  true .

 **Examples:** 

Muestra una alternativa añadida a la renderización de mapa de bits y cambia el tipo de advertencias sobre registros de metarchivo no compatibles.

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
boolean - Un valor que determina si las operaciones raster deben emularse o no.
### getEmulateRenderingToSizeOnPage() {#getEmulateRenderingToSizeOnPage}
```
public boolean getEmulateRenderingToSizeOnPage()
```


Obtiene un valor que determina si el renderizado del metafichero emula la visualización del metafichero según el tamaño en la página o la visualización del metafichero en su tamaño predeterminado.

 **Remarks:** 

Cuando los metaficheros se muestran en MS Word, algunos gráficos pueden escalarse según el tamaño real del metafichero en píxeles. Es decir, incluso el zoom puede afectar la visualización del metafichero.

Cuando este valor se establece en  true , **Aspose.Words** emula el renderizado de acuerdo con el tamaño del metafichero en la página. El tamaño en píxeles se calcula a partir del tamaño del metafichero en la página y el especificado [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Cuando este valor se establece en  false , **Aspose.Words** emula el renderizado del metafichero a su tamaño predeterminado en píxeles.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo visualizar el metafichero según el tamaño en la página.

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
boolean - Un valor que determina si el renderizado del metafichero emula la visualización del metafichero según el tamaño en la página o la visualización del metafichero en su tamaño predeterminado.
### getEmulateRenderingToSizeOnPageResolution() {#getEmulateRenderingToSizeOnPageResolution}
```
public int getEmulateRenderingToSizeOnPageResolution()
```


Obtiene la resolución en píxeles por pulgada para la emulación del renderizado del metafichero al tamaño en la página.

 **Remarks:** 

Esta opción se usa solo cuando [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) está establecido en  true .

El valor predeterminado es 96. Esta es una resolución de visualización predeterminada. Es decir, el renderizado del metafichero emulará la visualización del metafichero en MS Word con un factor de zoom del 100%.

 **Examples:** 

Muestra cómo visualizar el metafichero según el tamaño en la página.

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
int - La resolución en píxeles por pulgada para la emulación del renderizado del metafichero al tamaño en la página.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


Obtiene un valor que determina cómo se deben renderizar las imágenes del metafichero.

 **Remarks:** 

El valor predeterminado depende del formato de guardado. Para imágenes es [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Para otros formatos es [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Muestra una alternativa añadida a la renderización de mapa de bits y cambia el tipo de advertencias sobre registros de metarchivo no compatibles.

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
int - Un valor que determina cómo deben renderizarse las imágenes de metafichero. El valor devuelto es una de las constantes de [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/).
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


Obtiene un valor que determina cómo se deben renderizar los metaficheros WMF con metaficheros EMF incrustados.

 **Remarks:** 

Los metaficheros WMF pueden contener datos EMF incrustados. MS Word, en la mayoría de los casos, usa datos EMF incrustados. GDI+ siempre usa datos WMF.

Cuando este valor se establece en  true , **Aspose.Words** usa datos EMF incrustados al renderizar.

Cuando este valor se establece en  false , **Aspose.Words** usa datos WMF al renderizar.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales. Cuando el metafichero se renderiza a mapa de bits, siempre se usan datos WMF.

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo configurar las opciones de renderizado relacionadas con Enhanced Windows Metafile al guardar en PDF.

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
boolean - Un valor que determina cómo deben renderizarse los metaficheros WMF con metaficheros EMF incrustados.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


Obtiene un valor que determina si se debe usar GDI+ para la emulación de operaciones raster o no.

 **Remarks:** 

La biblioteca Windows GDI+ podría usarse para emular operaciones raster. Proporciona soporte para todas las operaciones raster en comparación con la propia emulación de **Aspose.Words**, pero el rendimiento puede ser más lento en algunos casos.

Cuando este valor se establece en  true , **Aspose.Words** usa GDI+ para la emulación de operaciones raster.

Cuando este valor se establece en  false , **Aspose.Words** usa su propia implementación de la emulación de operaciones raster.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo establecer el modo de renderizado al guardar documentos con imágenes Windows Metafile en otros formatos de imagen.

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
boolean - Un valor que determina si se debe o no usar GDI+ para la emulación de operaciones raster.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


Establece un valor que determina cómo se deben renderizar los metaficheros EMF+ Dual.

 **Remarks:** 

Los metaficheros EMF+ Dual contienen tanto partes EMF+ como EMF. MS Word y GDI+ siempre renderizan la parte EMF+. Aspose.Words actualmente no soporta completamente todos los registros EMF+ y, en algunos casos, el resultado del renderizado de la parte EMF se ve mejor que el resultado del renderizado de la parte EMF+.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales. Cuando el metafichero se renderiza a bitmap, siempre se usa la parte EMF+.

El valor predeterminado es [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

 **Examples:** 

Muestra cómo configurar las opciones de renderizado relacionadas con Enhanced Windows Metafile al guardar en PDF.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un valor que determina cómo deben renderizarse los metafiles EMF+ Dual. El valor debe ser una de las constantes de [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/). |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


Establece un valor que determina si se deben emular o no las operaciones raster.

 **Remarks:** 

Se pueden usar operaciones raster específicas en los metaficheros. No pueden renderizarse directamente a gráficos vectoriales. Emular operaciones raster requiere una rasterización parcial de los gráficos vectoriales resultantes, lo que puede afectar el rendimiento de renderizado del metafichero.

Cuando este valor se establece en  true , **Aspose.Words** emula las operaciones raster. La salida resultante puede estar parcialmente rasterizada y el rendimiento podría ser más lento.

Cuando este valor se establece en  false , **Aspose.Words** no emula las operaciones raster. Cuando **Aspose.Words** encuentra una operación raster en un metafichero, recurre a renderizar el metafichero en un mapa de bits utilizando el sistema operativo.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es  true .

 **Examples:** 

Muestra una alternativa añadida a la renderización de mapa de bits y cambia el tipo de advertencias sobre registros de metarchivo no compatibles.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que determina si las operaciones raster deben ser emuladas o no. |

### setEmulateRenderingToSizeOnPage(boolean value) {#setEmulateRenderingToSizeOnPage-boolean}
```
public void setEmulateRenderingToSizeOnPage(boolean value)
```


Establece un valor que determina si el renderizado del metafichero emula la visualización del metafichero según el tamaño en la página o la visualización del metafichero en su tamaño predeterminado.

 **Remarks:** 

Cuando los metaficheros se muestran en MS Word, algunos gráficos pueden escalarse según el tamaño real del metafichero en píxeles. Es decir, incluso el zoom puede afectar la visualización del metafichero.

Cuando este valor se establece en  true , **Aspose.Words** emula el renderizado de acuerdo con el tamaño del metafichero en la página. El tamaño en píxeles se calcula a partir del tamaño del metafichero en la página y el especificado [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Cuando este valor se establece en  false , **Aspose.Words** emula el renderizado del metafichero a su tamaño predeterminado en píxeles.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo visualizar el metafichero según el tamaño en la página.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que determina si el renderizado del metafile emula la visualización del metafile según el tamaño en la página o la visualización del metafile en su tamaño predeterminado. |

### setEmulateRenderingToSizeOnPageResolution(int value) {#setEmulateRenderingToSizeOnPageResolution-int}
```
public void setEmulateRenderingToSizeOnPageResolution(int value)
```


Establece la resolución en píxeles por pulgada para la emulación del renderizado del metafichero al tamaño en la página.

 **Remarks:** 

Esta opción se usa solo cuando [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) está establecido en  true .

El valor predeterminado es 96. Esta es una resolución de visualización predeterminada. Es decir, el renderizado del metafichero emulará la visualización del metafichero en MS Word con un factor de zoom del 100%.

 **Examples:** 

Muestra cómo visualizar el metafichero según el tamaño en la página.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | La resolución en píxeles por pulgada para la emulación del renderizado del metafile al tamaño en la página. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


Establece un valor que determina cómo se deben renderizar las imágenes del metafichero.

 **Remarks:** 

El valor predeterminado depende del formato de guardado. Para imágenes es [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Para otros formatos es [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Muestra una alternativa añadida a la renderización de mapa de bits y cambia el tipo de advertencias sobre registros de metarchivo no compatibles.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un valor que determina cómo deben renderizarse las imágenes de metafile. El valor debe ser una de las constantes de [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/). |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Establece un valor que determina cómo se deben renderizar los metaficheros WMF con metaficheros EMF incrustados.

 **Remarks:** 

Los metaficheros WMF pueden contener datos EMF incrustados. MS Word, en la mayoría de los casos, usa datos EMF incrustados. GDI+ siempre usa datos WMF.

Cuando este valor se establece en  true , **Aspose.Words** usa datos EMF incrustados al renderizar.

Cuando este valor se establece en  false , **Aspose.Words** usa datos WMF al renderizar.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales. Cuando el metafichero se renderiza a mapa de bits, siempre se usan datos WMF.

El valor predeterminado es  true .

 **Examples:** 

Muestra cómo configurar las opciones de renderizado relacionadas con Enhanced Windows Metafile al guardar en PDF.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que determina cómo deben renderizarse los metafiles WMF con metafiles EMF incrustados. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


Establece un valor que determina si se debe usar GDI+ para la emulación de operaciones raster o no.

 **Remarks:** 

La biblioteca Windows GDI+ podría usarse para emular operaciones raster. Proporciona soporte para todas las operaciones raster en comparación con la propia emulación de **Aspose.Words**, pero el rendimiento puede ser más lento en algunos casos.

Cuando este valor se establece en  true , **Aspose.Words** usa GDI+ para la emulación de operaciones raster.

Cuando este valor se establece en  false , **Aspose.Words** usa su propia implementación de la emulación de operaciones raster.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo establecer el modo de renderizado al guardar documentos con imágenes Windows Metafile en otros formatos de imagen.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que determina si se debe o no usar GDI+ para la emulación de operaciones raster. |

