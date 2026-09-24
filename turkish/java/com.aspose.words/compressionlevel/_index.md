---
title: "CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Aspose.Words Java için"
description: "Java'da OOXML ve XPS dosyaları için sıkıştırma seviyesi."
type: docs
weight: 122
url: /tr/java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

OOXML ve XPS dosyaları için sıkıştırma seviyesi.

(DOCX, DOTX ve XPS dosyaları dahili olarak bir ZIP arşivi, bu özellik arşivin sıkıştırma seviyesini kontrol eder.

Not, FlatOpc dosyasının bir ZIP arşivi olmadığını, bu nedenle bu özelliğin FlatOpc dosyalarını etkilemediğini belirtir.)

 **Examples:** 

OOXML belgesi kaydedilirken kullanılacak sıkıştırma seviyesinin nasıl belirtileceğini gösterir.

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

Bir belge XPS formatında kaydedilirken sıkıştırma seviyesinin nasıl kontrol edileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample document for XPS compression test.");

 // Create an XpsSaveOptions object and set the compression level.
 XpsSaveOptions options = new XpsSaveOptions();
 options.setCompressionLevel(CompressionLevel.MAXIMUM);

 doc.save(getArtifactsDir() + "XpsSaveOptions.CompressionLevelXps.xps", options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FAST](#FAST) | Hızlı sıkıştırma seviyesi. |
| [MAXIMUM](#MAXIMUM) | Maksimum sıkıştırma seviyesi. |
| [NORMAL](#NORMAL) | Normal sıkıştırma seviyesi. |
| [SUPER_FAST](#SUPER-FAST) | Süper Hızlı sıkıştırma seviyesi. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compressionLevel)](#toString-int) |  |
### FAST {#FAST}
```
public static int FAST
```


Hızlı sıkıştırma seviyesi.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Maksimum sıkıştırma seviyesi.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal sıkıştırma seviyesi. Aspose.Words tarafından kullanılan varsayılan sıkıştırma seviyesi.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Süper Hızlı sıkıştırma seviyesi. Microsoft Word bu sıkıştırma seviyesini kullanır.

### length {#length}
```
public static int length
```


### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
