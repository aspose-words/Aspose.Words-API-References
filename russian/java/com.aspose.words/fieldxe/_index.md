---
title: FieldXE
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле XE.
type: docs
weight: 262
url: /ru/java/com.aspose.words/fieldxe/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldXE extends Field
```

Реализует поле XE.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Определяет текст и номер страницы для элемента индекса, который используется полем ИНДЕКС.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getEntryType()](#getEntryType--) | Получает тип записи индекса. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getPageNumberReplacement()](#getPageNumberReplacement--) | Получает текст, используемый вместо номера страницы. |
| [getPageRangeBookmarkName()](#getPageRangeBookmarkName--) | Получает имя закладки, помечающей диапазон страниц, который вставляется в качестве номера страницы записи. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getText()](#getText--) | Получает текст записи. |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [getYomi()](#getYomi--) | Получает ёми (первый фонетический символ для сортировки индексов) для записи индекса |
| [hashCode()](#hashCode--) |  |
| [isBold()](#isBold--) | Определяет, следует ли применять полужирное форматирование к номеру страницы записи. |
| [isBold(boolean value)](#isBold-boolean-) | Устанавливает, следует ли применять полужирное форматирование к номеру страницы записи. |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isItalic()](#isItalic--) | Определяет, следует ли применять курсивное форматирование к номеру страницы записи. |
| [isItalic(boolean value)](#isItalic-boolean-) | Устанавливает, следует ли применять курсивное форматирование к номеру страницы записи. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setEntryType(String value)](#setEntryType-java.lang.String-) | Задает тип записи индекса. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setPageNumberReplacement(String value)](#setPageNumberReplacement-java.lang.String-) | Устанавливает текст, используемый вместо номера страницы. |
| [setPageRangeBookmarkName(String value)](#setPageRangeBookmarkName-java.lang.String-) | Задает имя закладки, помечающей диапазон страниц, который вставляется в качестве номера страницы записи. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setText(String value)](#setText-java.lang.String-) | Устанавливает текст записи. |
| [setYomi(String value)](#setYomi-java.lang.String-) | Устанавливает ёми (первый фонетический символ для сортировки индексов) для записи индекса |
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
### getEntryType() {#getEntryType--}
```
public String getEntryType()
```


Получает тип записи индекса.

**Возвращает:**
java.lang.String — тип записи индекса.
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
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getPageNumberReplacement() {#getPageNumberReplacement--}
```
public String getPageNumberReplacement()
```


Получает текст, используемый вместо номера страницы.

**Возвращает:**
java.lang.String — текст, используемый вместо номера страницы.
### getPageRangeBookmarkName() {#getPageRangeBookmarkName--}
```
public String getPageRangeBookmarkName()
```


Получает имя закладки, помечающей диапазон страниц, который вставляется в качестве номера страницы записи.

**Возвращает:**
java.lang.String — имя закладки, помечающей диапазон страниц, который вставляется как номер страницы записи.
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
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Получает узел, представляющий начало поля.

**Возвращает:**
[FieldStart](../../com.aspose.words/fieldstart) - Узел, представляющий начало поля.
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
### getText() {#getText--}
```
public String getText()
```


Получает текст записи.

**Возвращает:**
java.lang.String — текст записи.
### getType() {#getType--}
```
public int getType()
```


Получает тип поля Microsoft Word.

**Возвращает:**
 int — тип поля Microsoft Word. Возвращаемое значение является одним из[FieldType](../../com.aspose.words/fieldtype) константы.
### getYomi() {#getYomi--}
```
public String getYomi()
```


Получает ёми (первый фонетический символ для сортировки индексов) для записи индекса

**Возвращает:**
java.lang.String — ёми (первый фонетический символ для сортировки индексов) для записи индекса
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isBold() {#isBold--}
```
public boolean isBold()
```


Определяет, следует ли применять полужирное форматирование к номеру страницы записи.

**Возвращает:**
boolean — применять ли полужирное форматирование к номеру страницы записи.
### isBold(boolean value) {#isBold-boolean-}
```
public void isBold(boolean value)
```


Устанавливает, следует ли применять полужирное форматирование к номеру страницы записи.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли применять полужирное форматирование к номеру страницы записи. |

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

### isItalic() {#isItalic--}
```
public boolean isItalic()
```


Определяет, следует ли применять курсивное форматирование к номеру страницы записи.

**Возвращает:**
boolean — применять ли курсив к номеру страницы записи.
### isItalic(boolean value) {#isItalic-boolean-}
```
public void isItalic(boolean value)
```


Устанавливает, следует ли применять курсивное форматирование к номеру страницы записи.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли применять курсив к номеру страницы записи. |

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
### setEntryType(String value) {#setEntryType-java.lang.String-}
```
public void setEntryType(String value)
```


Задает тип записи индекса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Тип записи индекса. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setPageNumberReplacement(String value) {#setPageNumberReplacement-java.lang.String-}
```
public void setPageNumberReplacement(String value)
```


Устанавливает текст, используемый вместо номера страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, используемый вместо номера страницы. |

### setPageRangeBookmarkName(String value) {#setPageRangeBookmarkName-java.lang.String-}
```
public void setPageRangeBookmarkName(String value)
```


Задает имя закладки, помечающей диапазон страниц, который вставляется в качестве номера страницы записи.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя закладки, помечающей диапазон страниц, который вставляется в качестве номера страницы записи. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Устанавливает текст записи.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст записи. |

### setYomi(String value) {#setYomi-java.lang.String-}
```
public void setYomi(String value)
```


Устанавливает ёми (первый фонетический символ для сортировки индексов) для записи индекса

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Ёми (первый фонетический символ для сортировки указателей) для элемента указателя |

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
