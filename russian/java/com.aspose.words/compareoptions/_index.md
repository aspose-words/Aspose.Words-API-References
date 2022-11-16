---
title: CompareOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет выбрать дополнительные параметры для операции сравнения документов.
type: docs
weight: 81
url: /ru/java/com.aspose.words/compareoptions/
---

**Наследование:**
java.lang.Object
```
public class CompareOptions
```

Позволяет выбрать дополнительные параметры для операции сравнения документов.

 Чтобы узнать больше, посетите**Compare Documents** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getGranularity()](#getGranularity--) | Указывает, отслеживаются ли изменения по символам или по словам. |
| [getIgnoreCaseChanges()](#getIgnoreCaseChanges--) | True указывает, что сравнение документов нечувствительно к регистру. |
| [getIgnoreComments()](#getIgnoreComments--) | Указывает, следует ли сравнивать различия в комментариях. |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId--) | Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. |
| [getIgnoreFields()](#getIgnoreFields--) | Указывает, следует ли сравнивать различия в полях. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes--) | Указывает, следует ли сравнивать различия в сносках и концевых сносках. |
| [getIgnoreFormatting()](#getIgnoreFormatting--) | True указывает, что форматирование игнорируется. |
| [getIgnoreHeadersAndFooters()](#getIgnoreHeadersAndFooters--) | True указывает, что содержимое верхних и нижних колонтитулов игнорируется. |
| [getIgnoreTables()](#getIgnoreTables--) | Указывает, следует ли сравнивать различия в данных, содержащихся в таблицах. |
| [getIgnoreTextboxes()](#getIgnoreTextboxes--) | Указывает, следует ли сравнивать различия в данных, содержащихся в текстовых полях. |
| [getTarget()](#getTarget--) | Указывает, какой документ должен использоваться в качестве эталона при сравнении. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setGranularity(int value)](#setGranularity-int-) | Указывает, отслеживаются ли изменения по символам или по словам. |
| [setIgnoreCaseChanges(boolean value)](#setIgnoreCaseChanges-boolean-) | True указывает, что сравнение документов нечувствительно к регистру. |
| [setIgnoreComments(boolean value)](#setIgnoreComments-boolean-) | Указывает, следует ли сравнивать различия в комментариях. |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean-) | Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean-) | Указывает, следует ли сравнивать различия в полях. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean-) | Указывает, следует ли сравнивать различия в сносках и концевых сносках. |
| [setIgnoreFormatting(boolean value)](#setIgnoreFormatting-boolean-) | True указывает, что форматирование игнорируется. |
| [setIgnoreHeadersAndFooters(boolean value)](#setIgnoreHeadersAndFooters-boolean-) | True указывает, что содержимое верхних и нижних колонтитулов игнорируется. |
| [setIgnoreTables(boolean value)](#setIgnoreTables-boolean-) | Указывает, следует ли сравнивать различия в данных, содержащихся в таблицах. |
| [setIgnoreTextboxes(boolean value)](#setIgnoreTextboxes-boolean-) | Указывает, следует ли сравнивать различия в данных, содержащихся в текстовых полях. |
| [setTarget(int value)](#setTarget-int-) | Указывает, какой документ должен использоваться в качестве эталона при сравнении. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getGranularity() {#getGranularity--}
```
public int getGranularity()
```


 Указывает, отслеживаются ли изменения по символам или по словам. Значение по умолчанию[Granularity.WORD\_LEVEL](../../com.aspose.words/granularity\#WORD-LEVEL).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[Granularity](../../com.aspose.words/granularity) константы.
### getIgnoreCaseChanges() {#getIgnoreCaseChanges--}
```
public boolean getIgnoreCaseChanges()
```


True указывает, что сравнение документов нечувствительно к регистру. По умолчанию сравнение чувствительно к регистру.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreComments() {#getIgnoreComments--}
```
public boolean getIgnoreComments()
```


Указывает, следует ли сравнивать различия в комментариях. По умолчанию комментарии не игнорируются.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId--}
```
public boolean getIgnoreDmlUniqueId()
```


 Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreFields() {#getIgnoreFields--}
```
public boolean getIgnoreFields()
```


Указывает, следует ли сравнивать различия в полях. По умолчанию поля не игнорируются.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreFootnotes() {#getIgnoreFootnotes--}
```
public boolean getIgnoreFootnotes()
```


Указывает, следует ли сравнивать различия в сносках и концевых сносках. По умолчанию сноски не игнорируются.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreFormatting() {#getIgnoreFormatting--}
```
public boolean getIgnoreFormatting()
```


True указывает, что форматирование игнорируется. По умолчанию форматирование документа не игнорируется.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreHeadersAndFooters() {#getIgnoreHeadersAndFooters--}
```
public boolean getIgnoreHeadersAndFooters()
```


True указывает, что содержимое верхних и нижних колонтитулов игнорируется. По умолчанию верхние и нижние колонтитулы не игнорируются.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreTables() {#getIgnoreTables--}
```
public boolean getIgnoreTables()
```


Указывает, следует ли сравнивать различия в данных, содержащихся в таблицах. По умолчанию таблицы не игнорируются.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreTextboxes() {#getIgnoreTextboxes--}
```
public boolean getIgnoreTextboxes()
```


Указывает, следует ли сравнивать различия в данных, содержащихся в текстовых полях. По умолчанию текстовые поля не игнорируются.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTarget() {#getTarget--}
```
public int getTarget()
```


Указывает, какой документ должен использоваться в качестве эталона при сравнении.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ComparisonTargetType](../../com.aspose.words/comparisontargettype) константы.
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




### setGranularity(int value) {#setGranularity-int-}
```
public void setGranularity(int value)
```


 Указывает, отслеживаются ли изменения по символам или по словам. Значение по умолчанию[Granularity.WORD\_LEVEL](../../com.aspose.words/granularity\#WORD-LEVEL).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[Granularity](../../com.aspose.words/granularity) константы. |

### setIgnoreCaseChanges(boolean value) {#setIgnoreCaseChanges-boolean-}
```
public void setIgnoreCaseChanges(boolean value)
```


True указывает, что сравнение документов нечувствительно к регистру. По умолчанию сравнение чувствительно к регистру.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreComments(boolean value) {#setIgnoreComments-boolean-}
```
public void setIgnoreComments(boolean value)
```


Указывает, следует ли сравнивать различия в комментариях. По умолчанию комментарии не игнорируются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean-}
```
public void setIgnoreDmlUniqueId(boolean value)
```


 Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean-}
```
public void setIgnoreFields(boolean value)
```


Указывает, следует ли сравнивать различия в полях. По умолчанию поля не игнорируются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean-}
```
public void setIgnoreFootnotes(boolean value)
```


Указывает, следует ли сравнивать различия в сносках и концевых сносках. По умолчанию сноски не игнорируются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreFormatting(boolean value) {#setIgnoreFormatting-boolean-}
```
public void setIgnoreFormatting(boolean value)
```


True указывает, что форматирование игнорируется. По умолчанию форматирование документа не игнорируется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreHeadersAndFooters(boolean value) {#setIgnoreHeadersAndFooters-boolean-}
```
public void setIgnoreHeadersAndFooters(boolean value)
```


True указывает, что содержимое верхних и нижних колонтитулов игнорируется. По умолчанию верхние и нижние колонтитулы не игнорируются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreTables(boolean value) {#setIgnoreTables-boolean-}
```
public void setIgnoreTables(boolean value)
```


Указывает, следует ли сравнивать различия в данных, содержащихся в таблицах. По умолчанию таблицы не игнорируются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreTextboxes(boolean value) {#setIgnoreTextboxes-boolean-}
```
public void setIgnoreTextboxes(boolean value)
```


Указывает, следует ли сравнивать различия в данных, содержащихся в текстовых полях. По умолчанию текстовые поля не игнорируются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setTarget(int value) {#setTarget-int-}
```
public void setTarget(int value)
```


Указывает, какой документ должен использоваться в качестве эталона при сравнении.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ComparisonTargetType](../../com.aspose.words/comparisontargettype) константы. |

### toString() {#toString--}
```
public String toString()
```




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
