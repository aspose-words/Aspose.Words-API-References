---
title: "SdtCalendarType"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words для Java"
description: "Указывает возможные типы календарей, которые могут использоваться для указания StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint в документе Office Open XML на Java."
type: docs
weight: 600
url: /ru/java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Указывает возможные типы календарей, которые могут использоваться для указания [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/\#setCalendarType-int) в документе Office Open XML.

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
| [DEFAULT](#DEFAULT) | Используется как значение по умолчанию в OOXML. |
| [GREGORIAN](#GREGORIAN) | Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. |
| [GREGORIAN_US](#GREGORIAN-US) | Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. |
| [HEBREW](#HEBREW) | Указывает, что следует использовать еврейский лунный календарь, описанный формулой Гаусса для Песаха [CITATION] и полным изложением устного закона (Мишне Тора). |
| [HIJRI](#HIJRI) | Указывает, что следует использовать исламский лунный календарь, описанный Королевством Саудовская Аравия, Министерством исламских дел, имуществом, Da\u2018wah и руководством. |
| [JAPAN](#JAPAN) | Указывает, что следует использовать календарь эпохи японского императора, описанный Японским промышленным стандартом JIS X 0301. |
| [KOREA](#KOREA) | Указывает, что следует использовать календарь эпохи корейского Тангуна, описанный корейским законом №. |
| [NONE](#NONE) | Указывает, что календарь использовать не следует. |
| [SAKA](#SAKA) | Указывает, что следует использовать календарь эпохи Сака, описанный Комитетом реформы календаря Индии, как часть Индийского эфемеридного и морского альманаха. |
| [TAIWAN](#TAIWAN) | Указывает, что следует использовать тайваньский календарь, определённый китайским национальным стандартом CNS 7648. |
| [THAI](#THAI) | Указывает, что следует использовать тайский календарь, определённый Королевским указом Его Высочества. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Используется как значение по умолчанию в OOXML. Равно [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. Этот календарь должен быть локализован на соответствующий язык.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. Значения этого календаря должны быть представлены на арабском.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. Значения этого календаря должны быть представлены на французском для Ближнего Востока.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. Значения этого календаря должны быть представлены на английском.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. Значения этого календаря должны представлять английские строки соответствующими арабскими символами (арабская транслитерация английского названия григорианского календаря).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


Указывает, что следует использовать григорианский календарь, определённый в ISO 8601. Значения этого календаря должны представлять французские строки соответствующими арабскими символами (арабская транслитерация французского названия григорианского календаря).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Указывает, что следует использовать еврейский лунный календарь, описанный формулой Гаусса для Песаха [CITATION] и полным изложением устного закона (Мишне Тора).

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Указывает, что следует использовать исламский лунный календарь, описанный Королевством Саудовская Аравия, Министерством исламских дел, имуществом, Da\u2018wah и руководством.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Указывает, что следует использовать календарь эпохи японского императора, описанный Японским промышленным стандартом JIS X 0301.

### KOREA {#KOREA}
```
public static int KOREA
```


Указывает, что следует использовать календарь эпохи корейского Тангуна, описанный корейским законом № 4.

### NONE {#NONE}
```
public static int NONE
```


Указывает, что календарь использовать не следует.

 **Remarks:** 

Обычно в AW значение None является первым и значением по умолчанию для перечислений, но в данном случае это не так. None не является значением по умолчанию для OOXML, вместо этого [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN) является значением по умолчанию и первым членом этого перечисления.

### SAKA {#SAKA}
```
public static int SAKA
```


Указывает, что следует использовать календарь эпохи Сака, описанный Комитетом реформы календаря Индии, как часть Индийского эфемеридного и морского альманаха.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Указывает, что следует использовать тайваньский календарь, определённый китайским национальным стандартом CNS 7648.

### THAI {#THAI}
```
public static int THAI
```


Указывает, что следует использовать тайский календарь, определённый Королевским указом Его Высочества короля Ваджиравуда (Рама VI) в Королевском вестнике B. E. 2456 (1913 г.) и указом премьер‑министра Пибунсонгкрам (1941 г.), который устанавливает начало года с 1 января по григорианскому календарю и сопоставляет нулевой год с григорианским 543 г. до н.э., следует использовать.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtCalendarType) {#toString-int}
```
public static String toString(int sdtCalendarType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
