---
title: FieldDatabase
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле DATABASE.
type: docs
weight: 174
url: /ru/java/com.aspose.words/fielddatabase/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldDatabase extends Field
```

Реализует поле DATABASE.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Вставляет результаты запроса к базе данных в таблицу WordprocessingML.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getConnection()](#getConnection--) | Получает соединение с данными. |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFileName()](#getFileName--) | Получает полный путь и имя файла базы данных |
| [getFirstRecord()](#getFirstRecord--) | Получает целочисленный номер записи первой записи данных для вставки. |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getFormatAttributes()](#getFormatAttributes--) | Получает, какие атрибуты формата должны быть применены к таблице. |
| [getInsertHeadings()](#getInsertHeadings--) | Определяет, вставлять ли имена полей из базы данных в качестве заголовков столбцов в результирующую таблицу. |
| [getInsertOnceOnMailMerge()](#getInsertOnceOnMailMerge--) | Получает, следует ли вставлять данные в начале слияния. |
| [getLastRecord()](#getLastRecord--) | Получает целочисленный номер последней вставляемой записи данных. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getQuery()](#getQuery--) | Получает набор инструкций SQL, которые запрашивают базу данных. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getTableFormat()](#getTableFormat--) | Получает формат, который должен быть применен к результату запроса к базе данных. |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setConnection(String value)](#setConnection-java.lang.String-) | Устанавливает соединение с данными. |
| [setFileName(String value)](#setFileName-java.lang.String-) | Устанавливает полный путь и имя файла базы данных |
| [setFirstRecord(String value)](#setFirstRecord-java.lang.String-) | Устанавливает целочисленный номер записи первой записи данных для вставки. |
| [setFormatAttributes(String value)](#setFormatAttributes-java.lang.String-) | Устанавливает, какие атрибуты формата должны применяться к таблице. |
| [setInsertHeadings(boolean value)](#setInsertHeadings-boolean-) | Устанавливает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующую таблицу. |
| [setInsertOnceOnMailMerge(boolean value)](#setInsertOnceOnMailMerge-boolean-) | Устанавливает, следует ли вставлять данные в начале слияния. |
| [setLastRecord(String value)](#setLastRecord-java.lang.String-) | Задает целочисленный номер последней вставляемой записи данных. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setQuery(String value)](#setQuery-java.lang.String-) | Задает набор инструкций SQL, которые запрашивают базу данных. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setTableFormat(String value)](#setTableFormat-java.lang.String-) | Задает формат, который должен применяться к результату запроса к базе данных. |
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
### getConnection() {#getConnection--}
```
public String getConnection()
```


Получает соединение с данными.

**Возвращает:**
java.lang.String — подключение к данным.
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
### getFileName() {#getFileName--}
```
public String getFileName()
```


Получает полный путь и имя файла базы данных

**Возвращает:**
java.lang.String — полный путь и имя файла базы данных
### getFirstRecord() {#getFirstRecord--}
```
public String getFirstRecord()
```


Получает целочисленный номер записи первой записи данных для вставки.

**Возвращает:**
java.lang.String — целочисленный номер первой записи данных для вставки.
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля.

**Возвращает:**
[FieldFormat](../../com.aspose.words/fieldformat) - А[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля.
### getFormatAttributes() {#getFormatAttributes--}
```
public String getFormatAttributes()
```


Получает, какие атрибуты формата должны быть применены к таблице.

**Возвращает:**
java.lang.String — Какие атрибуты формата должны применяться к таблице.
### getInsertHeadings() {#getInsertHeadings--}
```
public boolean getInsertHeadings()
```


Определяет, вставлять ли имена полей из базы данных в качестве заголовков столбцов в результирующую таблицу.

**Возвращает:**
boolean — следует ли вставлять имена полей из базы данных в качестве заголовков столбцов результирующей таблицы.
### getInsertOnceOnMailMerge() {#getInsertOnceOnMailMerge--}
```
public boolean getInsertOnceOnMailMerge()
```


Получает, следует ли вставлять данные в начале слияния.

**Возвращает:**
boolean — вставлять ли данные в начале слияния.
### getLastRecord() {#getLastRecord--}
```
public String getLastRecord()
```


Получает целочисленный номер последней вставляемой записи данных.

**Возвращает:**
java.lang.String — целочисленный номер последней вставляемой записи данных.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getQuery() {#getQuery--}
```
public String getQuery()
```


Получает набор инструкций SQL, которые запрашивают базу данных.

**Возвращает:**
java.lang.String — набор инструкций SQL, которые запрашивают базу данных.
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
### getTableFormat() {#getTableFormat--}
```
public String getTableFormat()
```


Получает формат, который должен быть применен к результату запроса к базе данных.

**Возвращает:**
java.lang.String — формат, который должен применяться к результату запроса к базе данных.
### getType() {#getType--}
```
public int getType()
```


Получает тип поля Microsoft Word.

**Возвращает:**
 int — тип поля Microsoft Word. Возвращаемое значение является одним из[FieldType](../../com.aspose.words/fieldtype) константы.
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
### setConnection(String value) {#setConnection-java.lang.String-}
```
public void setConnection(String value)
```


Устанавливает соединение с данными.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Связь с данными. |

### setFileName(String value) {#setFileName-java.lang.String-}
```
public void setFileName(String value)
```


Устанавливает полный путь и имя файла базы данных

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Полный путь и имя файла базы данных |

### setFirstRecord(String value) {#setFirstRecord-java.lang.String-}
```
public void setFirstRecord(String value)
```


Устанавливает целочисленный номер записи первой записи данных для вставки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Целый номер записи первой записи данных для вставки. |

### setFormatAttributes(String value) {#setFormatAttributes-java.lang.String-}
```
public void setFormatAttributes(String value)
```


Устанавливает, какие атрибуты формата должны применяться к таблице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Какие атрибуты формата должны применяться к таблице. |

### setInsertHeadings(boolean value) {#setInsertHeadings-boolean-}
```
public void setInsertHeadings(boolean value)
```


Устанавливает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующую таблицу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли имена полей из базы данных в качестве заголовков столбцов в результирующую таблицу. |

### setInsertOnceOnMailMerge(boolean value) {#setInsertOnceOnMailMerge-boolean-}
```
public void setInsertOnceOnMailMerge(boolean value)
```


Устанавливает, следует ли вставлять данные в начале слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли данные в начале слияния. |

### setLastRecord(String value) {#setLastRecord-java.lang.String-}
```
public void setLastRecord(String value)
```


Задает целочисленный номер последней вставляемой записи данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Целый номер записи последней записи данных для вставки. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setQuery(String value) {#setQuery-java.lang.String-}
```
public void setQuery(String value)
```


Задает набор инструкций SQL, которые запрашивают базу данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Набор инструкций SQL, которые запрашивают базу данных. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setTableFormat(String value) {#setTableFormat-java.lang.String-}
```
public void setTableFormat(String value)
```


Задает формат, который должен применяться к результату запроса к базе данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Формат, который должен применяться к результату запроса к базе данных. |

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
