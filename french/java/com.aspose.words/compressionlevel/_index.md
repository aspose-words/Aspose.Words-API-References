---
title: "CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Aspose.Words pour Java"
description: "Niveau de compression pour les fichiers OOXML et XPS en Java."
type: docs
weight: 122
url: /fr/java/com.aspose.words/compressionlevel/
---

**Inheritance:**
java.lang.Object
```
public class CompressionLevel
```

Niveau de compression pour les fichiers OOXML et XPS.

(Les fichiers DOCX, DOTX et XPS sont internement une archive ZIP, cette propriété contrôle le niveau de compression de l'archive.

Remarque, le fichier FlatOpc n'est pas une archive ZIP, par conséquent, cette propriété n'affecte pas les fichiers FlatOpc.)

 **Examples:** 

Montre comment spécifier le niveau de compression à utiliser lors de l'enregistrement d'un document OOXML.

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

Montre comment contrôler le niveau de compression lors de l'enregistrement d'un document au format XPS.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample document for XPS compression test.");

 // Create an XpsSaveOptions object and set the compression level.
 XpsSaveOptions options = new XpsSaveOptions();
 options.setCompressionLevel(CompressionLevel.MAXIMUM);

 doc.save(getArtifactsDir() + "XpsSaveOptions.CompressionLevelXps.xps", options);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [FAST](#FAST) | Niveau de compression rapide. |
| [MAXIMUM](#MAXIMUM) | Niveau de compression maximal. |
| [NORMAL](#NORMAL) | Niveau de compression normal. |
| [SUPER_FAST](#SUPER-FAST) | Niveau de compression super rapide. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String compressionLevelName)](#fromName-java.lang.String) |  |
| [getName(int compressionLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compressionLevel)](#toString-int) |  |
### FAST {#FAST}
```
public static int FAST
```


Niveau de compression rapide.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Niveau de compression maximal.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Niveau de compression normal. Niveau de compression par défaut utilisé par Aspose.Words.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Niveau de compression super rapide. Microsoft Word utilise ce niveau de compression.

### length {#length}
```
public static int length
```


### fromName(String compressionLevelName) {#fromName-java.lang.String}
```
public static int fromName(String compressionLevelName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Returns:**
int
### getName(int compressionLevel) {#getName-int}
```
public static String getName(int compressionLevel)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| compressionLevel | int |  |

**Returns:**
java.lang.String
