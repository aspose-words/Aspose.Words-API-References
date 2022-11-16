---
title: FieldSeq
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле SEQ.
type: docs
weight: 241
url: /ru/java/com.aspose.words/fieldseq/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldSeq extends Field
```

Реализует поле SEQ.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Последовательная нумерация глав, таблиц, рисунков и других определяемых пользователем списков элементов в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | Получает имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении. |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getInsertNextNumber()](#getInsertNextNumber--) | Определяет, нужно ли вставлять следующий порядковый номер для указанного элемента. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getResetHeadingLevel()](#getResetHeadingLevel--) | Получает целое число, представляющее уровень заголовка, на который нужно сбросить порядковый номер. |
| [getResetNumber()](#getResetNumber--) | Получает целое число для сброса порядкового номера. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getSequenceIdentifier()](#getSequenceIdentifier--) | Получает имя, присвоенное серии элементов, которые должны быть пронумерованы. |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Задает имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении. |
| [setInsertNextNumber(boolean value)](#setInsertNextNumber-boolean-) | Устанавливает, следует ли вставлять следующий порядковый номер для указанного элемента. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setResetHeadingLevel(String value)](#setResetHeadingLevel-java.lang.String-) | Задает целое число, представляющее уровень заголовка, на который сбрасывается порядковый номер. |
| [setResetNumber(String value)](#setResetNumber-java.lang.String-) | Устанавливает целое число для сброса порядкового номера. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setSequenceIdentifier(String value)](#setSequenceIdentifier-java.lang.String-) | Устанавливает имя, присвоенное серии элементов, которые должны быть пронумерованы. |
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
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


Получает имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении.

**Возвращает:**
java.lang.String — имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении.
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
### getInsertNextNumber() {#getInsertNextNumber--}
```
public boolean getInsertNextNumber()
```


Определяет, нужно ли вставлять следующий порядковый номер для указанного элемента.

**Возвращает:**
boolean — вставлять ли следующий порядковый номер для указанного элемента.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getResetHeadingLevel() {#getResetHeadingLevel--}
```
public String getResetHeadingLevel()
```


Получает целое число, представляющее уровень заголовка, на который нужно сбросить порядковый номер. Возвращает -1, если число отсутствует.

**Возвращает:**
java.lang.String — Целое число, представляющее уровень заголовка, на который нужно сбросить порядковый номер.
### getResetNumber() {#getResetNumber--}
```
public String getResetNumber()
```


Получает целое число для сброса порядкового номера. Возвращает -1, если число отсутствует.

**Возвращает:**
java.lang.String — целое число, на которое нужно сбросить порядковый номер.
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
### getSequenceIdentifier() {#getSequenceIdentifier--}
```
public String getSequenceIdentifier()
```


Получает имя, присвоенное серии элементов, которые должны быть пронумерованы.

**Возвращает:**
java.lang.String — имя, присвоенное серии элементов, которые должны быть пронумерованы.
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
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


Задает имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении. |

### setInsertNextNumber(boolean value) {#setInsertNextNumber-boolean-}
```
public void setInsertNextNumber(boolean value)
```


Устанавливает, следует ли вставлять следующий порядковый номер для указанного элемента.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли следующий порядковый номер для указанного элемента. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setResetHeadingLevel(String value) {#setResetHeadingLevel-java.lang.String-}
```
public void setResetHeadingLevel(String value)
```


Задает целое число, представляющее уровень заголовка, на который сбрасывается порядковый номер. Возвращает -1, если число отсутствует.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Целое число, представляющее уровень заголовка для сброса порядкового номера. |

### setResetNumber(String value) {#setResetNumber-java.lang.String-}
```
public void setResetNumber(String value)
```


Устанавливает целое число для сброса порядкового номера. Возвращает -1, если число отсутствует.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Целое число для сброса порядкового номера. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setSequenceIdentifier(String value) {#setSequenceIdentifier-java.lang.String-}
```
public void setSequenceIdentifier(String value)
```


Устанавливает имя, присвоенное серии элементов, которые должны быть пронумерованы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя, присвоенное серии элементов, которые должны быть пронумерованы. |

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
