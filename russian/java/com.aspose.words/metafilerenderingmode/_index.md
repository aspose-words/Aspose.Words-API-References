---
title: "MetafileRenderingMode"
linktitle: "MetafileRenderingMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как Aspose.Words должен рендерить метафайлы WMF и EMF в Java."
type: docs
weight: 467
url: /ru/java/com.aspose.words/metafilerenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingMode
```

Указывает, как Aspose.Words должен отображать метафайлы WMF и EMF.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BITMAP](#BITMAP) | Aspose.Words вызывает GDI+ для рендеринга метафайла в bitmap, а затем сохраняет bitmap в выходной документ. |
| [VECTOR](#VECTOR) | Aspose.Words рендерит метафайл как векторную графику. |
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | Aspose.Words пытается рендерить метафайл как векторную графику. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int metafileRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int metafileRenderingMode)](#toString-int) |  |
### BITMAP {#BITMAP}
```
public static int BITMAP
```


Aspose.Words вызывает GDI+ для рендеринга метафайла в bitmap, а затем сохраняет bitmap в выходной документ.

### VECTOR {#VECTOR}
```
public static int VECTOR
```


Aspose.Words рендерит метафайл как векторную графику.

### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


Aspose.Words пытается рендерить метафайл как векторную графику. Если Aspose.Words не может корректно отрендерить некоторые записи метафайла в векторную графику, то Aspose.Words рендерит этот метафайл в bitmap.

### length {#length}
```
public static int length
```


### fromName(String metafileRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String metafileRenderingModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int metafileRenderingMode) {#getName-int}
```
public static String getName(int metafileRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**Returns:**
java.lang.String
