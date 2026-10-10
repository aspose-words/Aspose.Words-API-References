---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se combina el formato al combinar varios documentos en Java."
type: docs
weight: 464
url: /es/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

Especifica cómo se combina el formato al combinar varios documentos.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Significa que el documento de origen conservará su formato original, como estilos de fuente, tamaños, colores, sangrías y cualquier otro elemento de formato aplicado a su contenido. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | Conserve el diseño de los documentos originales en el documento final. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | Combine el formato de los documentos combinados. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Significa que el documento de origen conservará su formato original, como estilos de fuente, tamaños, colores, sangrías y cualquier otro elemento de formato aplicado a su contenido.

 **Remarks:** 

Al usar esta opción, garantiza que el contenido copiado aparezca tal como lo hacía en la fuente original, sin importar la configuración de formato del primer documento en la cola de combinación.

Esta opción no tiene ningún efecto cuando los formatos de entrada y salida son PDF.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


Conserve el diseño de los documentos originales en el documento final.

 **Remarks:** 

En general, parece que imprime los documentos originales y los une manualmente con pegamento.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


Combine el formato de los documentos combinados.

 **Remarks:** 

Al usar esta opción, Aspose.Words adapta el formato del primer documento para que coincida con la estructura y apariencia del segundo documento, pero mantiene parte del formato original intacto. Esta opción es útil cuando desea mantener el aspecto general del documento de destino pero aún conservar ciertos aspectos de formato del documento original.

Esta opción no tiene ningún efecto cuando los formatos de entrada y salida son PDF.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
