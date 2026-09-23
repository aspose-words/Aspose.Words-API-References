---
title: "EmbeddedFontStyle"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words для Java"
description: "Указывает стиль встроенного шрифта внутри объекта FontInfo в Java."
type: docs
weight: 185
url: /ru/java/com.aspose.words/embeddedfontstyle/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontStyle
```

Указывает стиль встроенного шрифта внутри объекта [FontInfo](../../com.aspose.words/fontinfo/).

 **Examples:** 

Показывает, как извлечь встроенный шрифт из документа и сохранить его в локальную файловую систему.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BOLD](#BOLD) | Указывает встроенный полужирный шрифт. |
| [BOLD_ITALIC](#BOLD-ITALIC) | Указывает встроенный полужирный курсивный шрифт. |
| [ITALIC](#ITALIC) | Указывает встроенный курсивный шрифт. |
| [REGULAR](#REGULAR) | Указывает обычный встроенный шрифт. |
| [length](#length) |  |
## Методы

| Метод | Описание |
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


Указывает встроенный полужирный шрифт.

### BOLD_ITALIC {#BOLD-ITALIC}
```
public static int BOLD_ITALIC
```


Указывает встроенный полужирный курсивный шрифт.

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Указывает встроенный курсивный шрифт.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Указывает обычный встроенный шрифт.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontStyleName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontStyleName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontStyleName | java.lang.String |  |

**Returns:**
int
### fromNames(Set embeddedFontStyleNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set embeddedFontStyleNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontStyleNames | java.util.Set |  |

**Returns:**
int
### getName(int embeddedFontStyle) {#getName-int}
```
public static String getName(int embeddedFontStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### getNames(int embeddedFontStyle) {#getNames-int}
```
public static Set getNames(int embeddedFontStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
