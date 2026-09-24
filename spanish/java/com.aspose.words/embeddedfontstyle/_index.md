---
title: "EmbeddedFontStyle"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words para Java"
description: "Especifica el estilo de una fuente incrustada dentro de un objeto FontInfo en Java."
type: docs
weight: 185
url: /es/java/com.aspose.words/embeddedfontstyle/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontStyle
```

Especifica el estilo de una fuente incrustada dentro de un objeto [FontInfo](../../com.aspose.words/fontinfo/).

 **Examples:** 

Muestra cómo extraer una fuente incrustada de un documento y guardarla en el sistema de archivos local.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BOLD](#BOLD) | Especifica la fuente incrustada en negrita. |
| [BOLD_ITALIC](#BOLD-ITALIC) | Especifica la fuente incrustada en negrita cursiva. |
| [ITALIC](#ITALIC) | Especifica la fuente incrustada en cursiva. |
| [REGULAR](#REGULAR) | Especifica la fuente incrustada regular. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
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


Especifica la fuente incrustada en negrita.

### BOLD_ITALIC {#BOLD-ITALIC}
```
public static int BOLD_ITALIC
```


Especifica la fuente incrustada en negrita cursiva.

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Especifica la fuente incrustada en cursiva.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Especifica la fuente incrustada regular.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontStyleName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontStyleName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| embeddedFontStyleName | java.lang.String |  |

**Returns:**
int
### fromNames(Set embeddedFontStyleNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set embeddedFontStyleNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| embeddedFontStyleNames | java.util.Set |  |

**Returns:**
int
### getName(int embeddedFontStyle) {#getName-int}
```
public static String getName(int embeddedFontStyle)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### getNames(int embeddedFontStyle) {#getNames-int}
```
public static Set getNames(int embeddedFontStyle)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
