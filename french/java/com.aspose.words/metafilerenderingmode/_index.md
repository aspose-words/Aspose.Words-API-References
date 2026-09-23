---
title: "MetafileRenderingMode"
linktitle: "MetafileRenderingMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment Aspose.Words doit rendre les métafichiers WMF et EMF en Java."
type: docs
weight: 467
url: /fr/java/com.aspose.words/metafilerenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingMode
```

Spécifie comment Aspose.Words doit rendre les métafichiers WMF et EMF.

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
## Champs

| Champ | Description |
| --- | --- |
| [BITMAP](#BITMAP) | Aspose.Words invoque GDI+ pour rendre un métafichier en bitmap, puis enregistre le bitmap dans le document de sortie. |
| [VECTOR](#VECTOR) | Aspose.Words rend un métafichier sous forme de graphiques vectoriels. |
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | Aspose.Words tente de rendre un métafichier sous forme de graphiques vectoriels. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int metafileRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int metafileRenderingMode)](#toString-int) |  |
### BITMAP {#BITMAP}
```
public static int BITMAP
```


Aspose.Words invoque GDI+ pour rendre un métafichier en bitmap, puis enregistre le bitmap dans le document de sortie.

### VECTOR {#VECTOR}
```
public static int VECTOR
```


Aspose.Words rend un métafichier sous forme de graphiques vectoriels.

### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


Aspose.Words tente de rendre un métafichier sous forme de graphiques vectoriels. Si Aspose.Words ne peut pas rendre correctement certains enregistrements du métafichier en graphiques vectoriels, alors Aspose.Words rend ce métafichier en bitmap.

### length {#length}
```
public static int length
```


### fromName(String metafileRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String metafileRenderingModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int metafileRenderingMode) {#getName-int}
```
public static String getName(int metafileRenderingMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
