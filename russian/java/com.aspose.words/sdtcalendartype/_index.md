---
title: SdtCalendarType
second_title: Справочник по API Aspose.Words для Java
description: Указывает возможные типы календарей, которые можно использовать для указания / в документе Office Open XML.
type: docs
weight: 504
url: /ru/java/com.aspose.words/sdtcalendartype/
---

**Наследование:**
java.lang.Object
```
public class SdtCalendarType
```

 Определяет возможные типы календарей, которые можно использовать для указания[StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag\#getCalendarType--) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag\#setCalendarType-int-) в документе Office Open XML.
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Используется как значение по умолчанию в OOXML. |
| [GREGORIAN](#GREGORIAN) | Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. |
| [GREGORIAN_US](#GREGORIAN-US) | Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. |
| [HEBREW](#HEBREW) |  Указывает, что еврейский лунный календарь, описанный формулой Гаусса для Песаха[ЦИТАТА] и «Полное изложение устного закона» (Мишне Тора). |
| [HIJRI](#HIJRI) | Указывает, что лунный календарь хиджры, описанный Королевством Саудовская Аравия, Министерством по делам ислама, пожертвованиями, Да\\u2018wah и Guidance. |
| [JAPAN](#JAPAN) | Указывает, что должен использоваться календарь эпохи японского императора, как описано в японском промышленном стандарте JIS X 0301. |
| [KOREA](#KOREA) | Указывает, что корейский календарь эры Тангун, как описано в Законе Кореи №. |
| [NONE](#NONE) | Указывает, что календарь не должен использоваться. |
| [SAKA](#SAKA) | Указывает, что должен использоваться календарь эпохи саков, описанный Комитетом по реформе календаря Индии, как часть Индийских эфемерид и Морского альманаха. |
| [TAIWAN](#TAIWAN) | Указывает, что должен использоваться тайваньский календарь, определенный китайским национальным стандартом CNS 7648. |
| [THAI](#THAI) | Указывает, что тайский календарь, определенный Королевским указом Его Величества |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int sdtCalendarType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int sdtCalendarType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


 Используется как значение по умолчанию в OOXML. Равно[GREGORIAN](../../com.aspose.words/sdtcalendartype\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. Этот календарь должен быть переведен на соответствующий язык.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. Значения для этого календаря должны быть представлены на арабском языке.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. Значения для этого календаря должны быть представлены на ближневосточном французском языке.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. Значения для этого календаря должны быть представлены на английском языке.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. Значения для этого календаря должны быть представлением английских строк соответствующими арабскими символами (арабская транслитерация английского языка для григорианского календаря).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


Указывает, что должен использоваться григорианский календарь, определенный в ISO 8601. Значения для этого календаря должны быть представлением французских строк соответствующими арабскими символами (арабская транслитерация французского языка для григорианского календаря).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


 Указывает, что еврейский лунный календарь, описанный формулой Гаусса для Песаха[ЦИТАТА] и «Полное изложение устного закона» (Мишне Тора).

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Указывает, что лунный календарь хиджры, описанный Королевством Саудовская Аравия, Министерством по делам ислама, пожертвованиями, Да\\u2018wah и Guidance.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Указывает, что должен использоваться календарь эпохи японского императора, как описано в японском промышленном стандарте JIS X 0301.

### KOREA {#KOREA}
```
public static int KOREA
```


Указывает, что должен использоваться корейский календарь эпохи Тангун, как описано в Законодательном акте Кореи № 4.

### NONE {#NONE}
```
public static int NONE
```


 Указывает, что календарь не должен использоваться. Обычно в AW None является первым и значением по умолчанию для перечислений, но не в этом случае. None не является значением по умолчанию для OOXML, вместо этого[GREGORIAN](../../com.aspose.words/sdtcalendartype\#GREGORIAN) по умолчанию и является первым членом этого перечисления.

### SAKA {#SAKA}
```
public static int SAKA
```


Указывает, что должен использоваться календарь эпохи саков, описанный Комитетом по реформе календаря Индии, как часть Индийских эфемерид и Морского альманаха.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Указывает, что должен использоваться тайваньский календарь, определенный китайским национальным стандартом CNS 7648.

### THAI {#THAI}
```
public static int THAI
```


Указывает, что тайский календарь, как это определено Королевским указом Его Величества короля Ваджиравуда (Рамы VI) в Королевской газете 2456 г. н.э. (1913 г. н.э.) и указом премьер-министра Фибунсонгхрама (1941 г. н.э.), начинать год по григорианскому календарю 1 января. и для сопоставления нулевого года с 543 годом до н.э. по григорианскому календарю.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String sdtCalendarTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int sdtCalendarType) {#getName-int-}
```
public static String getName(int sdtCalendarType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int sdtCalendarType) {#toString-int-}
```
public static String toString(int sdtCalendarType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
