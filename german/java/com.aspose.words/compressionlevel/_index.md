---
title: "CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Aspose.Words für Java"
description: "Komprimierungsstufe für OOXML- und XPS-Dateien in Java."
type: docs
weight: 122
url: /de/java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

Komprimierungsstufe für OOXML- und XPS-Dateien.

(DOCX-, DOTX- und XPS-Dateien sind intern ein ZIP-Archiv, diese Eigenschaft steuert die Komprimierungsstufe des Archivs.

Hinweis, dass die FlatOpc-Datei kein ZIP-Archiv ist, daher wirkt sich diese Eigenschaft nicht auf die FlatOpc-Dateien aus.)

 **Examples:** 

Zeigt, wie die beim Speichern eines OOXML-Dokuments zu verwendende Komprimierungsstufe angegeben wird.

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

Zeigt, wie die Komprimierungsstufe beim Speichern eines Dokuments im XPS-Format gesteuert wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample document for XPS compression test.");

 // Create an XpsSaveOptions object and set the compression level.
 XpsSaveOptions options = new XpsSaveOptions();
 options.setCompressionLevel(CompressionLevel.MAXIMUM);

 doc.save(getArtifactsDir() + "XpsSaveOptions.CompressionLevelXps.xps", options);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FAST](#FAST) | Schnelle Komprimierungsstufe. |
| [MAXIMUM](#MAXIMUM) | Maximale Komprimierungsstufe. |
| [NORMAL](#NORMAL) | Normale Komprimierungsstufe. |
| [SUPER_FAST](#SUPER-FAST) | Superschnelle Komprimierungsstufe. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compressionLevel)](#toString-int) |  |
### FAST {#FAST}
```
public static int FAST
```


Schnelle Komprimierungsstufe.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Maximale Komprimierungsstufe.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normale Komprimierungsstufe. Standardkomprimierungsstufe, die von Aspose.Words verwendet wird.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Superschnelle Komprimierungsstufe. Microsoft Word verwendet diese Komprimierungsstufe.

### length {#length}
```
public static int length
```


### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
