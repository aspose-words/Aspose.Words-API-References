---
title: "MetafileRenderingMode"
linktitle: "MetafileRenderingMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo Aspose.Words debe renderizar los metarchivos WMF y EMF en Java."
type: docs
weight: 467
url: /es/java/com.aspose.words/metafilerenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingMode
```

Especifica cómo Aspose.Words debe renderizar los metaficheros WMF y EMF.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BITMAP](#BITMAP) | Aspose.Words invoca GDI+ para renderizar un metarchivo a un mapa de bits y luego guarda el mapa de bits en el documento de salida. |
| [VECTOR](#VECTOR) | Aspose.Words renderiza un metarchivo como gráficos vectoriales. |
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | Aspose.Words intenta renderizar un metarchivo como gráficos vectoriales. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int metafileRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int metafileRenderingMode)](#toString-int) |  |
### BITMAP {#BITMAP}
```
public static int BITMAP
```


Aspose.Words invoca GDI+ para renderizar un metarchivo a un mapa de bits y luego guarda el mapa de bits en el documento de salida.

### VECTOR {#VECTOR}
```
public static int VECTOR
```


Aspose.Words renderiza un metarchivo como gráficos vectoriales.

### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


Aspose.Words intenta renderizar un metarchivo como gráficos vectoriales. Si Aspose.Words no puede renderizar correctamente algunos de los registros del metarchivo a gráficos vectoriales, entonces Aspose.Words renderiza este metarchivo a un mapa de bits.

### length {#length}
```
public static int length
```


### fromName(String metafileRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String metafileRenderingModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int metafileRenderingMode) {#getName-int}
```
public static String getName(int metafileRenderingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
