---
title: "SdtDateStorageFormat"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words для Java"
description: "Указывает, как дата для date SDT хранится/извлекается, когда SDT привязан к узлу XML в хранилище данных документа в Java."
type: docs
weight: 601
url: /ru/java/com.aspose.words/sdtdatestorageformat/
---

**Inheritance:**
java.lang.Object
```
public class SdtDateStorageFormat
```

Указывает, как дата для SDT типа «date» хранится/извлекается, когда SDT привязан к узлу XML в хранилище данных документа.

 **Examples:** 

Показывает, как запросить у пользователя ввод даты с помощью структурного тега документа.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DATE](#DATE) | Значение даты для date SDT хранится как дата в стандартном формате XML Schema Date. |
| [DATE_TIME](#DATE-TIME) | Значение даты для date SDT хранится как дата в стандартном формате XML Schema DateTime. |
| [DEFAULT](#DEFAULT) | По умолчанию: [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME) |
| [TEXT](#TEXT) | Значение даты для date SDT хранится как текст. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String sdtDateStorageFormatName)](#fromName-java.lang.String) |  |
| [getName(int sdtDateStorageFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtDateStorageFormat)](#toString-int) |  |
### DATE {#DATE}
```
public static int DATE
```


Значение даты для date SDT хранится как дата в стандартном формате XML Schema Date.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


Значение даты для date SDT хранится как дата в стандартном формате XML Schema DateTime.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


По умолчанию: [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

### TEXT {#TEXT}
```
public static int TEXT
```


Значение даты для date SDT хранится как текст.

### length {#length}
```
public static int length
```


### fromName(String sdtDateStorageFormatName) {#fromName-java.lang.String}
```
public static int fromName(String sdtDateStorageFormatName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtDateStorageFormatName | java.lang.String |  |

**Returns:**
int
### getName(int sdtDateStorageFormat) {#getName-int}
```
public static String getName(int sdtDateStorageFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtDateStorageFormat) {#toString-int}
```
public static String toString(int sdtDateStorageFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
