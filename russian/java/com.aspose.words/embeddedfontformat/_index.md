---
title: "EmbeddedFontFormat"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words для Java"
description: "Указывает формат конкретного встроенного шрифта внутри объекта FontInfo в Java."
type: docs
weight: 184
url: /ru/java/com.aspose.words/embeddedfontformat/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontFormat
```

Указывает формат конкретного встроенного шрифта внутри объекта [FontInfo](../../com.aspose.words/fontinfo/).

При сохранении документа в файл записываются только встроенные шрифты соответствующего формата.

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
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | Указывает формат файла Embedded OpenType (EOT). |
| [OPEN_TYPE](#OPEN-TYPE) | Указывает шрифт, встроенный как простая копия файла шрифта OpenType (TrueType). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int embeddedFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontFormat)](#toString-int) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


Указывает формат файла Embedded OpenType (EOT).

Этот формат встроенных шрифтов используется в файлах DOC.

 **Remarks:** 

Смотрите http://www.w3.org/Submission/EOT для описания формата.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


Указывает шрифт, встроенный как простая копия файла шрифта OpenType (TrueType).

Этот формат встроенных шрифтов используется в формате Open Office XML, включая файлы DOCX.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontFormatName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int embeddedFontFormat) {#getName-int}
```
public static String getName(int embeddedFontFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
