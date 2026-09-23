---
title: "MetafileRenderingOptions"
linktitle: "MetafileRenderingOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier des options de rendu de métafichier supplémentaires en Java."
type: docs
weight: 468
url: /fr/java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Permet de spécifier des options supplémentaires de rendu des métafichiers.

Pour en savoir plus, consultez l'article de documentation [ Handling Windows Metafiles ][Handling Windows Metafiles].

 **Examples:** 

Affiche l’ajout d’une solution de repli vers le rendu bitmap et la modification du type d’avertissements concernant les enregistrements de métafichier non pris en charge.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | Obtient une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | Obtient une valeur déterminant si les opérations raster doivent être émulées. |
| [getEmulateRenderingToSizeOnPage()](#getEmulateRenderingToSizeOnPage) | Obtient une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier selon la taille sur la page ou l'affichage du métafichier à sa taille par défaut. |
| [getEmulateRenderingToSizeOnPageResolution()](#getEmulateRenderingToSizeOnPageResolution) | Obtient la résolution en pixels par pouce pour l'émulation du rendu du métafichier à la taille sur la page. |
| [getRenderingMode()](#getRenderingMode) | Obtient une valeur déterminant comment les images de métafichier doivent être rendues. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | Obtient une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | Obtient une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | Définit une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | Définit une valeur déterminant si les opérations raster doivent être émulées ou non. |
| [setEmulateRenderingToSizeOnPage(boolean value)](#setEmulateRenderingToSizeOnPage-boolean) | Définit une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier selon la taille sur la page ou l'affichage du métafichier à sa taille par défaut. |
| [setEmulateRenderingToSizeOnPageResolution(int value)](#setEmulateRenderingToSizeOnPageResolution-int) | Définit la résolution en pixels par pouce pour l'émulation du rendu du métafichier à la taille sur la page. |
| [setRenderingMode(int value)](#setRenderingMode-int) | Définit une valeur déterminant comment les images de métafichier doivent être rendues. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | Définit une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | Définit une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


Obtient une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus.

 **Remarks:** 

Les fichiers métas EMF+ Dual contiennent à la fois des parties EMF+ et EMF. MS Word et GDI+ rendent toujours la partie EMF+. Aspose.Words ne prend actuellement pas entièrement en charge tous les enregistrements EMF+ et, dans certains cas, le résultat du rendu de la partie EMF est meilleur que celui de la partie EMF+.

Cette option n'est utilisée que lorsque le métafichier est rendu sous forme de graphiques vectoriels. Lorsque le métafichier est rendu en bitmap, la partie EMF+ est toujours utilisée.

La valeur par défaut est [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

 **Examples:** 

Montre comment configurer les options de rendu liées aux Enhanced Windows Metafile lors de l’enregistrement en PDF.

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
int - Une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus. La valeur retournée est l'une des constantes [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/) .
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


Obtient une valeur déterminant si les opérations raster doivent être émulées.

 **Remarks:** 

Des opérations raster spécifiques peuvent être utilisées dans les métafichiers. Elles ne peuvent pas être rendues directement en graphiques vectoriels. L'émulation des opérations raster nécessite une rasterisation partielle des graphiques vectoriels résultants, ce qui peut affecter les performances de rendu du métafichier.

Lorsque cette valeur est définie sur  true , Aspose.Words émule les opérations raster. La sortie résultante peut être partiellement rasterisée et les performances peuvent être plus lentes.

Lorsque cette valeur est définie sur  false , Aspose.Words n'émule pas les opérations raster. Lorsqu'Aspose.Words rencontre une opération raster dans un métafichier, il revient au rendu du métafichier sous forme de bitmap en utilisant le système d'exploitation.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels.

La valeur par défaut est  true .

 **Examples:** 

Affiche l’ajout d’une solution de repli vers le rendu bitmap et la modification du type d’avertissements concernant les enregistrements de métafichier non pris en charge.

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
boolean - Une valeur déterminant si les opérations raster doivent être émules ou non.
### getEmulateRenderingToSizeOnPage() {#getEmulateRenderingToSizeOnPage}
```
public boolean getEmulateRenderingToSizeOnPage()
```


Obtient une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier selon la taille sur la page ou l'affichage du métafichier à sa taille par défaut.

 **Remarks:** 

Lorsque les métafichiers sont affichés dans MS Word, certains graphiques peuvent être mis à l'échelle en fonction de la taille réelle du métafichier en pixels. C’est‑à‑dire que même le zoom peut affecter l'affichage du métafichier.

Lorsque cette valeur est définie sur  true , Aspose.Words émule le rendu en fonction de la taille du métafichier sur la page. La taille en pixels est calculée à partir de la taille du métafichier sur la page et des méthodes spécifiées [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Lorsque cette valeur est définie sur  false , Aspose.Words émule le rendu du métafichier à sa taille par défaut en pixels.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels.

La valeur par défaut est  true .

 **Examples:** 

Montre comment afficher le métafichier en fonction de la taille sur la page.

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
boolean - Une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier selon la taille sur la page ou l'affichage du métafichier à sa taille par défaut.
### getEmulateRenderingToSizeOnPageResolution() {#getEmulateRenderingToSizeOnPageResolution}
```
public int getEmulateRenderingToSizeOnPageResolution()
```


Obtient la résolution en pixels par pouce pour l'émulation du rendu du métafichier à la taille sur la page.

 **Remarks:** 

Cette option n'est utilisée que lorsque [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) est définie sur  true .

La valeur par défaut est 96. Il s'agit d'une résolution d'affichage par défaut. C’est‑à‑dire que le rendu du métafichier émule l'affichage du métafichier dans MS Word avec un facteur de zoom de 100 %.

 **Examples:** 

Montre comment afficher le métafichier en fonction de la taille sur la page.

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
int - La résolution en pixels par pouce pour l'émulation du rendu du métafichier à la taille sur la page.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


Obtient une valeur déterminant comment les images de métafichier doivent être rendues.

 **Remarks:** 

La valeur par défaut dépend du format d'enregistrement. Pour les images, elle est [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Pour les autres formats, elle est [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Affiche l’ajout d’une solution de repli vers le rendu bitmap et la modification du type d’avertissements concernant les enregistrements de métafichier non pris en charge.

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
int - Une valeur déterminant comment les images de métafichier doivent être rendues. La valeur retournée est l'une des constantes [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/) .
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


Obtient une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus.

 **Remarks:** 

Les métafichiers WMF peuvent contenir des données EMF intégrées. MS Word utilise dans la plupart des cas des données EMF intégrées. GDI+ utilise toujours des données WMF.

Lorsque cette valeur est définie sur  true , Aspose.Words utilise les données EMF intégrées lors du rendu.

Lorsque cette valeur est définie sur  false , Aspose.Words utilise les données WMF lors du rendu.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels. Lorsque le métafichier est rendu en bitmap, les données WMF sont toujours utilisées.

La valeur par défaut est  true .

 **Examples:** 

Montre comment configurer les options de rendu liées aux Enhanced Windows Metafile lors de l’enregistrement en PDF.

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
boolean - Une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


Obtient une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster.

 **Remarks:** 

La bibliothèque Windows GDI+ peut être utilisée pour émuler les opérations raster. Elle offre une prise en charge de toutes les opérations raster comparée à l'émulation propre à Aspose.Words, mais les performances peuvent être plus lentes dans certains cas.

Lorsque cette valeur est définie sur  true , Aspose.Words utilise GDI+ pour l'émulation des opérations raster.

Lorsque cette valeur est définie sur  false , Aspose.Words utilise sa propre implémentation de l'émulation des opérations raster.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels.

La valeur par défaut est false.

 **Examples:** 

Montre comment définir le mode de rendu lors de l'enregistrement de documents contenant des images Windows Metafile vers d'autres formats d'image.

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
boolean - Une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


Définit une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus.

 **Remarks:** 

Les fichiers métas EMF+ Dual contiennent à la fois des parties EMF+ et EMF. MS Word et GDI+ rendent toujours la partie EMF+. Aspose.Words ne prend actuellement pas entièrement en charge tous les enregistrements EMF+ et, dans certains cas, le résultat du rendu de la partie EMF est meilleur que celui de la partie EMF+.

Cette option n'est utilisée que lorsque le métafichier est rendu sous forme de graphiques vectoriels. Lorsque le métafichier est rendu en bitmap, la partie EMF+ est toujours utilisée.

La valeur par défaut est [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

 **Examples:** 

Montre comment configurer les options de rendu liées aux Enhanced Windows Metafile lors de l’enregistrement en PDF.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus. La valeur doit être l'une des constantes [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/). |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


Définit une valeur déterminant si les opérations raster doivent être émulées ou non.

 **Remarks:** 

Des opérations raster spécifiques peuvent être utilisées dans les métafichiers. Elles ne peuvent pas être rendues directement en graphiques vectoriels. L'émulation des opérations raster nécessite une rasterisation partielle des graphiques vectoriels résultants, ce qui peut affecter les performances de rendu du métafichier.

Lorsque cette valeur est définie sur  true , Aspose.Words émule les opérations raster. La sortie résultante peut être partiellement rasterisée et les performances peuvent être plus lentes.

Lorsque cette valeur est définie sur  false , Aspose.Words n'émule pas les opérations raster. Lorsqu'Aspose.Words rencontre une opération raster dans un métafichier, il revient au rendu du métafichier sous forme de bitmap en utilisant le système d'exploitation.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels.

La valeur par défaut est  true .

 **Examples:** 

Affiche l’ajout d’une solution de repli vers le rendu bitmap et la modification du type d’avertissements concernant les enregistrements de métafichier non pris en charge.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur déterminant s'il faut ou non émuler les opérations raster. |

### setEmulateRenderingToSizeOnPage(boolean value) {#setEmulateRenderingToSizeOnPage-boolean}
```
public void setEmulateRenderingToSizeOnPage(boolean value)
```


Définit une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier selon la taille sur la page ou l'affichage du métafichier à sa taille par défaut.

 **Remarks:** 

Lorsque les métafichiers sont affichés dans MS Word, certains graphiques peuvent être mis à l'échelle en fonction de la taille réelle du métafichier en pixels. C’est‑à‑dire que même le zoom peut affecter l'affichage du métafichier.

Lorsque cette valeur est définie sur  true , Aspose.Words émule le rendu en fonction de la taille du métafichier sur la page. La taille en pixels est calculée à partir de la taille du métafichier sur la page et des méthodes spécifiées [getEmulateRenderingToSizeOnPageResolution()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPageResolution) / [setEmulateRenderingToSizeOnPageResolution(int)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPageResolution-int).

Lorsque cette valeur est définie sur  false , Aspose.Words émule le rendu du métafichier à sa taille par défaut en pixels.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels.

La valeur par défaut est  true .

 **Examples:** 

Montre comment afficher le métafichier en fonction de la taille sur la page.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur déterminant si le rendu du métafile émule l'affichage du métafile selon la taille sur la page ou l'affichage du métafile à sa taille par défaut. |

### setEmulateRenderingToSizeOnPageResolution(int value) {#setEmulateRenderingToSizeOnPageResolution-int}
```
public void setEmulateRenderingToSizeOnPageResolution(int value)
```


Définit la résolution en pixels par pouce pour l'émulation du rendu du métafichier à la taille sur la page.

 **Remarks:** 

Cette option n'est utilisée que lorsque [getEmulateRenderingToSizeOnPage()](../../com.aspose.words/metafilerenderingoptions/\#getEmulateRenderingToSizeOnPage) / [setEmulateRenderingToSizeOnPage(boolean)](../../com.aspose.words/metafilerenderingoptions/\#setEmulateRenderingToSizeOnPage-boolean) est définie sur  true .

La valeur par défaut est 96. Il s'agit d'une résolution d'affichage par défaut. C’est‑à‑dire que le rendu du métafichier émule l'affichage du métafichier dans MS Word avec un facteur de zoom de 100 %.

 **Examples:** 

Montre comment afficher le métafichier en fonction de la taille sur la page.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La résolution en pixels par pouce pour l'émulation du rendu du métafile à la taille sur la page. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


Définit une valeur déterminant comment les images de métafichier doivent être rendues.

 **Remarks:** 

La valeur par défaut dépend du format d'enregistrement. Pour les images, elle est [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). Pour les autres formats, elle est [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

 **Examples:** 

Affiche l’ajout d’une solution de repli vers le rendu bitmap et la modification du type d’avertissements concernant les enregistrements de métafichier non pris en charge.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Une valeur déterminant comment les images de métafile doivent être rendues. La valeur doit être l'une des constantes [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/). |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Définit une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus.

 **Remarks:** 

Les métafichiers WMF peuvent contenir des données EMF intégrées. MS Word utilise dans la plupart des cas des données EMF intégrées. GDI+ utilise toujours des données WMF.

Lorsque cette valeur est définie sur  true , Aspose.Words utilise les données EMF intégrées lors du rendu.

Lorsque cette valeur est définie sur  false , Aspose.Words utilise les données WMF lors du rendu.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels. Lorsque le métafichier est rendu en bitmap, les données WMF sont toujours utilisées.

La valeur par défaut est  true .

 **Examples:** 

Montre comment configurer les options de rendu liées aux Enhanced Windows Metafile lors de l’enregistrement en PDF.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


Définit une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster.

 **Remarks:** 

La bibliothèque Windows GDI+ peut être utilisée pour émuler les opérations raster. Elle offre une prise en charge de toutes les opérations raster comparée à l'émulation propre à Aspose.Words, mais les performances peuvent être plus lentes dans certains cas.

Lorsque cette valeur est définie sur  true , Aspose.Words utilise GDI+ pour l'émulation des opérations raster.

Lorsque cette valeur est définie sur  false , Aspose.Words utilise sa propre implémentation de l'émulation des opérations raster.

Cette option n'est utilisée que lorsque le métafichier est rendu en graphiques vectoriels.

La valeur par défaut est false.

 **Examples:** 

Montre comment définir le mode de rendu lors de l'enregistrement de documents contenant des images Windows Metafile vers d'autres formats d'image.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster. |

