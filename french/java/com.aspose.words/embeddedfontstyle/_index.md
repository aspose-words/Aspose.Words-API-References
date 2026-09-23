---
title: "EmbeddedFontStyle"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words pour Java"
description: "Spécifie le style d'une police intégrée à l'intérieur d'un objet FontInfo en Java."
type: docs
weight: 185
url: /fr/java/com.aspose.words/embeddedfontstyle/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontStyle
```

Spécifie le style d’une police incorporée à l’intérieur d’un objet [FontInfo](../../com.aspose.words/fontinfo/).

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
| [BOLD](#BOLD) | Spécifie la police incorporée en gras. |
| [BOLD_ITALIC](#BOLD-ITALIC) | Spécifie la police incorporée en gras-italique. |
| [ITALIC](#ITALIC) | Spécifie la police incorporée en italique. |
| [REGULAR](#REGULAR) | Spécifie la police incorporée normale. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String embeddedFontStyleName)](#fromName-java.lang.String) |  |
| [fromNames(Set embeddedFontStyleNames)](#fromNames-java.util.Set) |  |
| [getName(int embeddedFontStyle)](#getName-int) |  |
| [getNames(int embeddedFontStyle)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontStyle)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Spécifie la police incorporée en gras.

### BOLD_ITALIC {#BOLD-ITALIC}
```
public static int BOLD_ITALIC
```


Spécifie la police incorporée en gras-italique.

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Spécifie la police incorporée en italique.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Spécifie la police incorporée normale.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontStyleName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontStyleName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontStyleName | java.lang.String |  |

**Returns:**
int
### fromNames(Set embeddedFontStyleNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set embeddedFontStyleNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontStyleNames | java.util.Set |  |

**Returns:**
int
### getName(int embeddedFontStyle) {#getName-int}
```
public static String getName(int embeddedFontStyle)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### getNames(int embeddedFontStyle) {#getNames-int}
```
public static Set getNames(int embeddedFontStyle)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int embeddedFontStyle) {#toString-int}
```
public static String toString(int embeddedFontStyle)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
