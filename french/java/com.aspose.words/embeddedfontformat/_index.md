---
title: "EmbeddedFontFormat"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words pour Java"
description: "Spécifie le format d'une police incorporée particulière à l'intérieur de l'objet FontInfo en Java."
type: docs
weight: 184
url: /fr/java/com.aspose.words/embeddedfontformat/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontFormat
```

Spécifie le format d'une police incorporée particulière à l'intérieur de l'objet [FontInfo](../../com.aspose.words/fontinfo/).

Lors de l'enregistrement d'un document dans un fichier, seules les polices incorporées du format correspondant sont écrites.

 **Examples:** 

Montre comment extraire une police incorporée d'un document et l'enregistrer sur le système de fichiers local.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | Spécifie le format de fichier Embedded OpenType (EOT). |
| [OPEN_TYPE](#OPEN-TYPE) | Spécifie la police, incorporée comme copie brute du fichier de police OpenType (TrueType). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int embeddedFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontFormat)](#toString-int) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


Spécifie le format de fichier Embedded OpenType (EOT).

Ce format de polices incorporées est utilisé dans les fichiers DOC.

 **Remarks:** 

Voir http://www.w3.org/Submission/EOT pour la description du format.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


Spécifie la police, incorporée comme copie brute du fichier de police OpenType (TrueType).

Ce format de polices incorporées est utilisé dans le format Open Office XML, y compris les fichiers DOCX.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontFormatName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int embeddedFontFormat) {#getName-int}
```
public static String getName(int embeddedFontFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int embeddedFontFormat) {#toString-int}
```
public static String toString(int embeddedFontFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
