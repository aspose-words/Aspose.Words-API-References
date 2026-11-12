---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words для Java"
description: "Указывает, когда использовать расширения формата ZIP64 для файлов OOXML в Java."
type: docs
weight: 750
url: /ru/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

Указывает, когда использовать расширения формата ZIP64 для файлов OOXML.

 **Remarks:** 

Файл OOXML представляет собой ZIP-архив, у которого есть ограничение в 4 ГБ (2^32 байта) на несжатый размер файла, сжатый размер файла и общий размер архива, а также ограничение в 65 535 (2^16‑1) файлов в архиве. Расширения формата ZIP64 увеличивают эти ограничения до 2^64.

 **Examples:** 

Показывает, как использовать расширения формата ZIP64.

```

 Random random = new Random();
 DocumentBuilder builder = new DocumentBuilder();

 for (int i = 0; i < 10000; i++)
 {
     BufferedImage bmp = new BufferedImage(5, 5, BufferedImage.TYPE_INT_ARGB);
     Graphics2D g = bmp.createGraphics();
     g.setColor(new Color(random.nextInt(254), random.nextInt(254), random.nextInt(254)));
     g.drawImage(bmp, 0, 0, null);
     g.dispose();
     builder.insertImage(bmp);
 }

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setZip64Mode(Zip64Mode.ALWAYS);

 builder.getDocument().save(getArtifactsDir() + "OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ALWAYS](#ALWAYS) | Всегда используйте расширения формата ZIP64. |
| [IF_NECESSARY](#IF-NECESSARY) | При необходимости используйте расширения формата ZIP64. |
| [NEVER](#NEVER) | Не используйте расширения формата ZIP64. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Всегда используйте расширения формата ZIP64.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


При необходимости используйте расширения формата ZIP64.

### NEVER {#NEVER}
```
public static int NEVER
```


Не используйте расширения формата ZIP64.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zip64Mode) {#toString-int}
```
public static String toString(int zip64Mode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
