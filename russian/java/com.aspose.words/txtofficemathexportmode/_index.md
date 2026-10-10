---
title: "TxtOfficeMathExportMode"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как Aspose.Words экспортирует OfficeMath в SaveFormat.TEXT в Java."
type: docs
weight: 694
url: /ru/java/com.aspose.words/txtofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtOfficeMathExportMode
```

Указывает, как Aspose.Words экспортирует OfficeMath в [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT).

 **Examples:** 

Показывает, как экспортировать объект OfficeMath как LaTeX в TXT.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 TxtSaveOptions saveOptions = new TxtSaveOptions();
 saveOptions.setOfficeMathExportMode(TxtOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [LATEX](#LATEX) | Экспортировать OfficeMath как LaTeX. |
| [TEXT](#TEXT) | Экспортировать OfficeMath как обычный текст. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String txtOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int txtOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtOfficeMathExportMode)](#toString-int) |  |
### LATEX {#LATEX}
```
public static int LATEX
```


Экспортировать OfficeMath как LaTeX.

### TEXT {#TEXT}
```
public static int TEXT
```


Экспортировать OfficeMath как обычный текст.

### length {#length}
```
public static int length
```


### fromName(String txtOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtOfficeMathExportModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| txtOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtOfficeMathExportMode) {#getName-int}
```
public static String getName(int txtOfficeMathExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtOfficeMathExportMode) {#toString-int}
```
public static String toString(int txtOfficeMathExportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
