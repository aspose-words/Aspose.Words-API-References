---
title: "CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Aspose.Words para Java"
description: "Nivel de compresión para archivos OOXML y XPS en Java."
type: docs
weight: 122
url: /es/java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

Nivel de compresión para archivos OOXML y XPS.

(Los archivos DOCX, DOTX y XPS son internamente un archivo ZIP, esta propiedad controla el nivel de compresión del archivo.

Nota, que el archivo FlatOpc no es un archivo ZIP, por lo tanto, esta propiedad no afecta a los archivos FlatOpc.)

 **Examples:** 

Muestra cómo especificar el nivel de compresión a usar al guardar un documento OOXML.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "CompressionLevel" property to "CompressionLevel.Maximum" to apply the strongest and slowest compression.
 // Set the "CompressionLevel" property to "CompressionLevel.Normal" to apply
 // the default compression that Aspose.Words uses while saving OOXML documents.
 // Set the "CompressionLevel" property to "CompressionLevel.Fast" to apply a faster and weaker compression.
 // Set the "CompressionLevel" property to "CompressionLevel.SuperFast" to apply
 // the default compression that Microsoft Word uses.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.DOCX);
 saveOptions.setCompressionLevel(compressionLevel);

 StopWatch st = new StopWatch();
 st.start();
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
 st.stop();

 File fileInfo = new File(getArtifactsDir() + "OoxmlSaveOptions.DocumentCompression.docx");

 System.out.println(MessageFormat.format("Saving operation done using the \"{0}\" compression level:", compressionLevel));
 System.out.println(MessageFormat.format("\tDuration:\t{0}", st.getTime()));
 System.out.println(MessageFormat.format("\tFile Size:\t{0} bytes", fileInfo.length()));
 
```

Muestra cómo controlar el nivel de compresión al guardar un documento en formato XPS.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample document for XPS compression test.");

 // Create an XpsSaveOptions object and set the compression level.
 XpsSaveOptions options = new XpsSaveOptions();
 options.setCompressionLevel(CompressionLevel.MAXIMUM);

 doc.save(getArtifactsDir() + "XpsSaveOptions.CompressionLevelXps.xps", options);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [FAST](#FAST) | Nivel de compresión rápido. |
| [MAXIMUM](#MAXIMUM) | Nivel máximo de compresión. |
| [NORMAL](#NORMAL) | Nivel de compresión normal. |
| [SUPER_FAST](#SUPER-FAST) | Nivel de compresión súper rápido. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compressionLevel)](#toString-int) |  |
### FAST {#FAST}
```
public static int FAST
```


Nivel de compresión rápido.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Nivel máximo de compresión.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Nivel de compresión normal. Nivel de compresión predeterminado usado por Aspose.Words.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Nivel de compresión súper rápido. Microsoft Word usa este nivel de compresión.

### length {#length}
```
public static int length
```


### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int compressionLevel) {#toString-int}
```
public static String toString(int compressionLevel)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
