---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как текст документа анализируется для определения значений даты и времени в Java."
type: docs
weight: 742
url: /ru/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

Указывает, как текст документа анализируется для определения значений даты и времени.

 **Examples:** 

Показывает, как указать автоматическое определение формата даты и времени.

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Формат даты и времени, используемый в документе, определяется автоматически. |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | Сначала используется формат даты и времени, установленный для текущего потока, для разбора строковых значений. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Формат даты и времени, используемый в документе, определяется автоматически. Это может занять дополнительное время.

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


Сначала используется формат даты и времени, установленный для текущего потока, для разбора строковых значений. Если разбор не удался, пробуются другие распространённые форматы даты и времени.

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxDateTimeParsingMode) {#toString-int}
```
public static String toString(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
