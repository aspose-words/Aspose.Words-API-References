---
title: FieldCitation
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле CITATION.
type: docs
weight: 168
url: /ru/java/com.aspose.words/fieldcitation/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldCitation extends Field
```

Реализует поле CITATION.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

 Вставляет содержимое файла**Source** элемент с указанным**Tag** элемент с использованием библиографического стиля.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAnotherSourceTag()](#getAnotherSourceTag--) |  Получает значение, соответствующее**Tag** значение элемента другого источника для включения в цитату. |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getFormatLanguageId()](#getFormatLanguageId--) | Получает идентификатор языка, который используется в сочетании с указанным библиографическим стилем для форматирования цитаты в документе. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getPageNumber()](#getPageNumber--) | Получает номер страницы, связанный с цитатой. |
| [getPrefix()](#getPrefix--) | Получает префикс, который добавляется к цитате. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getSourceTag()](#getSourceTag--) |  Получает значение, соответствующее**Tag**значение элемента источника для вставки. |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSuffix()](#getSuffix--) | Получает суффикс, который добавляется к цитате. |
| [getSuppressAuthor()](#getSuppressAuthor--) | Получает информацию о том, скрыта ли информация об авторе из цитирования. |
| [getSuppressTitle()](#getSuppressTitle--) | Получает информацию о том, скрыта ли информация о заголовке из цитирования. |
| [getSuppressYear()](#getSuppressYear--) | Получает информацию о том, скрыта ли информация о годе из цитирования. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [getVolumeNumber()](#getVolumeNumber--) | Получает номер тома, связанный с цитатой. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setAnotherSourceTag(String value)](#setAnotherSourceTag-java.lang.String-) |  Устанавливает значение, соответствующее**Tag** значение элемента другого источника для включения в цитату. |
| [setFormatLanguageId(String value)](#setFormatLanguageId-java.lang.String-) | Задает идентификатор языка, который используется в сочетании с указанным библиографическим стилем для форматирования цитирования в документе. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setPageNumber(String value)](#setPageNumber-java.lang.String-) | Устанавливает номер страницы, связанный с цитатой. |
| [setPrefix(String value)](#setPrefix-java.lang.String-) | Устанавливает префикс, который добавляется к цитате. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setSourceTag(String value)](#setSourceTag-java.lang.String-) |  Устанавливает значение, соответствующее**Tag**значение элемента источника для вставки. |
| [setSuffix(String value)](#setSuffix-java.lang.String-) | Устанавливает суффикс, который добавляется к цитате. |
| [setSuppressAuthor(boolean value)](#setSuppressAuthor-boolean-) | Устанавливает, будет ли информация об авторе исключена из цитирования. |
| [setSuppressTitle(boolean value)](#setSuppressTitle-boolean-) | Устанавливает, будет ли информация заголовка скрыта от цитирования. |
| [setSuppressYear(boolean value)](#setSuppressYear-boolean-) | Устанавливает, будет ли информация о году подавлена из цитирования. |
| [setVolumeNumber(String value)](#setVolumeNumber-java.lang.String-) | Устанавливает номер тома, связанный с цитатой. |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | Выполняет развязку поля. |
| [update()](#update--) | Выполняет обновление поля. |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | Выполняет обновление поля. |
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
### getAnotherSourceTag() {#getAnotherSourceTag--}
```
public String getAnotherSourceTag()
```


 Получает значение, соответствующее**Tag** значение элемента другого источника для включения в цитату.

**Возвращает:**
java.lang.String — значение, соответствующее**Tag** значение элемента другого источника для включения в цитату.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


 Получает текст, представляющий отображаемый результат поля.[Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--) метод должен быть вызван, чтобы получить правильное значение для[FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) а также[FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) поля.

**Возвращает:**
java.lang.String — текст, представляющий результат отображаемого поля.
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


Получает узел, представляющий конец поля.

**Возвращает:**
[FieldEnd](../../com.aspose.words/fieldend) - Узел, представляющий конец поля.
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат дочерних полей.

**Возвращает:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ True, если должны быть включены коды дочерних полей. |

**Возвращает:**
java.lang.String
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля.

**Возвращает:**
[FieldFormat](../../com.aspose.words/fieldformat) - А[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля.
### getFormatLanguageId() {#getFormatLanguageId--}
```
public String getFormatLanguageId()
```


Получает идентификатор языка, который используется в сочетании с указанным библиографическим стилем для форматирования цитаты в документе.

**Возвращает:**
java.lang.String — идентификатор языка, который используется в сочетании с указанным библиографическим стилем для форматирования цитирования в документе.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getPageNumber() {#getPageNumber--}
```
public String getPageNumber()
```


Получает номер страницы, связанный с цитатой.

**Возвращает:**
java.lang.String — номер страницы, связанный с цитатой.
### getPrefix() {#getPrefix--}
```
public String getPrefix()
```


Получает префикс, который добавляется к цитате.

**Возвращает:**
java.lang.String — префикс, который добавляется к цитате.
### getResult() {#getResult--}
```
public String getResult()
```


Получает текст, который находится между разделителем полей и концом поля.

**Возвращает:**
java.lang.String — текст между разделителем полей и концом поля.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Получает узел, представляющий разделитель полей. Может быть нулевым.

**Возвращает:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - Узел, представляющий разделитель полей.
### getSourceTag() {#getSourceTag--}
```
public String getSourceTag()
```


 Получает значение, соответствующее**Tag**значение элемента источника для вставки.

**Возвращает:**
java.lang.String — значение, соответствующее**Tag**значение элемента источника для вставки.
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Получает узел, представляющий начало поля.

**Возвращает:**
[FieldStart](../../com.aspose.words/fieldstart) - Узел, представляющий начало поля.
### getSuffix() {#getSuffix--}
```
public String getSuffix()
```


Получает суффикс, который добавляется к цитате.

**Возвращает:**
java.lang.String — суффикс, который добавляется к цитате.
### getSuppressAuthor() {#getSuppressAuthor--}
```
public boolean getSuppressAuthor()
```


Получает информацию о том, скрыта ли информация об авторе из цитирования.

**Возвращает:**
boolean - Удаляется ли информация об авторе из цитирования.
### getSuppressTitle() {#getSuppressTitle--}
```
public boolean getSuppressTitle()
```


Получает информацию о том, скрыта ли информация о заголовке из цитирования.

**Возвращает:**
boolean - Удаляется ли информация заголовка из цитирования.
### getSuppressYear() {#getSuppressYear--}
```
public boolean getSuppressYear()
```


Получает информацию о том, скрыта ли информация о годе из цитирования.

**Возвращает:**
boolean - Удаляется ли информация о годе из цитирования.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Возвращает:**
инт
### getType() {#getType--}
```
public int getType()
```


Получает тип поля Microsoft Word.

**Возвращает:**
 int — тип поля Microsoft Word. Возвращаемое значение является одним из[FieldType](../../com.aspose.words/fieldtype) константы.
### getVolumeNumber() {#getVolumeNumber--}
```
public String getVolumeNumber()
```


Получает номер тома, связанный с цитатой.

**Возвращает:**
java.lang.String — номер тома, связанный с цитатой.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isDirty() {#isDirty--}
```
public boolean isDirty()
```


Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ.

**Возвращает:**
boolean - Является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ.
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |

### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Получает, заблокировано ли поле (не должно пересчитывать его результат).

**Возвращает:**
boolean - Заблокировано ли поле (не должно пересчитывать результат).
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Заблокировано ли поле (не должно пересчитывать свой результат). |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public Node remove()
```


 Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает**null**.

**Возвращает:**
[Node](../../com.aspose.words/node)
### setAnotherSourceTag(String value) {#setAnotherSourceTag-java.lang.String-}
```
public void setAnotherSourceTag(String value)
```


 Устанавливает значение, соответствующее**Tag** значение элемента другого источника для включения в цитату.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Значение, которое соответствует**Tag** значение элемента другого источника для включения в цитату. |

### setFormatLanguageId(String value) {#setFormatLanguageId-java.lang.String-}
```
public void setFormatLanguageId(String value)
```


Задает идентификатор языка, который используется в сочетании с указанным библиографическим стилем для форматирования цитирования в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Идентификатор языка, который используется в сочетании с указанным библиографическим стилем для форматирования цитаты в документе. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setPageNumber(String value) {#setPageNumber-java.lang.String-}
```
public void setPageNumber(String value)
```


Устанавливает номер страницы, связанный с цитатой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Номер страницы, связанный с цитатой. |

### setPrefix(String value) {#setPrefix-java.lang.String-}
```
public void setPrefix(String value)
```


Устанавливает префикс, который добавляется к цитате.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Префикс, который ставится перед цитатой. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setSourceTag(String value) {#setSourceTag-java.lang.String-}
```
public void setSourceTag(String value)
```


 Устанавливает значение, соответствующее**Tag**значение элемента источника для вставки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Значение, которое соответствует**Tag**значение элемента источника для вставки. |

### setSuffix(String value) {#setSuffix-java.lang.String-}
```
public void setSuffix(String value)
```


Устанавливает суффикс, который добавляется к цитате.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Суффикс, который добавляется к цитате. |

### setSuppressAuthor(boolean value) {#setSuppressAuthor-boolean-}
```
public void setSuppressAuthor(boolean value)
```


Устанавливает, будет ли информация об авторе исключена из цитирования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Исключается ли информация об авторе из цитирования. |

### setSuppressTitle(boolean value) {#setSuppressTitle-boolean-}
```
public void setSuppressTitle(boolean value)
```


Устанавливает, будет ли информация заголовка скрыта от цитирования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Удаляется ли информация заголовка из цитирования. |

### setSuppressYear(boolean value) {#setSuppressYear-boolean-}
```
public void setSuppressYear(boolean value)
```


Устанавливает, будет ли информация о году подавлена из цитирования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Удаляется ли информация о годе из цитирования. |

### setVolumeNumber(String value) {#setVolumeNumber-java.lang.String-}
```
public void setVolumeNumber(String value)
```


Устанавливает номер тома, связанный с цитатой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Номер тома, связанный с цитатой. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### unlink() {#unlink--}
```
public boolean unlink()
```


Выполняет развязку поля.

Заменяет поле самым последним результатом.

Некоторые поля, такие как поля XE (запись индекса) и поля SEQ (последовательность), нельзя разъединить.

**Возвращает:**
 логический -\{ True, если связь с полем отсутствует, иначе false.
### update() {#update--}
```
public void update()
```


Выполняет обновление поля. Выдает, если поле уже обновляется.

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


Выполняет обновление поля. Выдает, если поле уже обновляется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Если значение равно true, то прямое форматирование результата поля прекращается, независимо от переключателя MERGEFORMAT, в противном случае выполняется обычное обновление. |

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
