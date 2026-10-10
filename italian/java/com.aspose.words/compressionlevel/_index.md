---
title: "CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Aspose.Words per Java"
description: "Livello di compressione per i file OOXML e XPS in Java."
type: docs
weight: 122
url: /it/java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

Livello di compressione per i file OOXML e XPS.

(I file DOCX, DOTX e XPS sono internamente un archivio ZIP, questa proprietà controlla il livello di compressione dell'archivio.

Nota, che il file FlatOpc non è un archivio ZIP, quindi questa proprietà non influisce sui file FlatOpc.)

 **Examples:** 

Mostra come specificare il livello di compressione da utilizzare durante il salvataggio di un documento OOXML.

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

Mostra come controllare il livello di compressione quando si salva un documento in formato XPS.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample document for XPS compression test.");

 // Create an XpsSaveOptions object and set the compression level.
 XpsSaveOptions options = new XpsSaveOptions();
 options.setCompressionLevel(CompressionLevel.MAXIMUM);

 doc.save(getArtifactsDir() + "XpsSaveOptions.CompressionLevelXps.xps", options);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [FAST](#FAST) | Livello di compressione veloce. |
| [MAXIMUM](#MAXIMUM) | Livello di compressione massimo. |
| [NORMAL](#NORMAL) | Livello di compressione normale. |
| [SUPER_FAST](#SUPER-FAST) | Livello di compressione super veloce. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compressionLevel)](#toString-int) |  |
### FAST {#FAST}
```
public static int FAST
```


Livello di compressione veloce.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Livello di compressione massimo.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Livello di compressione normale. Livello di compressione predefinito utilizzato da Aspose.Words.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Livello di compressione super veloce. Microsoft Word utilizza questo livello di compressione.

### length {#length}
```
public static int length
```


### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
