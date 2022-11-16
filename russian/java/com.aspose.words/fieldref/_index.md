---
title: FieldRef
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле REF.
type: docs
weight: 235
url: /ru/java/com.aspose.words/fieldref/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldRef extends Field
```

Реализует поле REF.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Вставляет текст или графику, представленную указанной закладкой.
## Методы

| Метод | Описание |
| --- | --- |
| [canWorkAsMergeField()](#canWorkAsMergeField--) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | Получает имя закладки, на которую указывает ссылка. |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getIncludeNoteOrComment()](#getIncludeNoteOrComment--) | Определяет, следует ли увеличивать номера сносок, концевых сносок и аннотаций, отмеченных закладкой, и вставлять соответствующие сноски, концевые сноски и текст комментариев. |
| [getInsertHyperlink()](#getInsertHyperlink--) | Получает, следует ли создавать гиперссылку на отмеченный закладкой абзац. |
| [getInsertParagraphNumber()](#getInsertParagraphNumber--) | Получает, следует ли вставлять номер абзаца указанного абзаца точно так, как он отображается в документе. |
| [getInsertParagraphNumberInFullContext()](#getInsertParagraphNumberInFullContext--) | Определяет, следует ли вставлять номер абзаца указанного абзаца в полный контекст. |
| [getInsertParagraphNumberInRelativeContext()](#getInsertParagraphNumberInRelativeContext--) | Определяет, вставлять ли номер абзаца ссылочного абзаца в относительный контекст. |
| [getInsertRelativePosition()](#getInsertRelativePosition--) | Получает, следует ли вставить относительное положение абзаца, на который делается ссылка. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getMergeFieldName()](#getMergeFieldName--) |  |
| [getNumberSeparator()](#getNumberSeparator--) | Получает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSuppressNonDelimiters()](#getSuppressNonDelimiters--) | Определяет, нужно ли подавлять символы, не являющиеся разделителями. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [isMergeValueRequired()](#isMergeValueRequired--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Устанавливает имя закладки, на которую указывает ссылка. |
| [setIncludeNoteOrComment(boolean value)](#setIncludeNoteOrComment-boolean-) | Устанавливает, следует ли увеличивать сноску, концевую сноску и аннотацию, отмеченные закладкой, и вставлять соответствующую сноску, концевую сноску и текст комментария. |
| [setInsertHyperlink(boolean value)](#setInsertHyperlink-boolean-) | Устанавливает, следует ли создавать гиперссылку на отмеченный закладкой абзац. |
| [setInsertParagraphNumber(boolean value)](#setInsertParagraphNumber-boolean-) | Устанавливает, следует ли вставлять номер абзаца ссылочного абзаца точно так, как он отображается в документе. |
| [setInsertParagraphNumberInFullContext(boolean value)](#setInsertParagraphNumberInFullContext-boolean-) | Устанавливает, вставлять ли номер абзаца ссылочного абзаца в полный контекст. |
| [setInsertParagraphNumberInRelativeContext(boolean value)](#setInsertParagraphNumberInRelativeContext-boolean-) | Устанавливает, вставлять ли номер абзаца ссылочного абзаца в относительный контекст. |
| [setInsertRelativePosition(boolean value)](#setInsertRelativePosition-boolean-) | Устанавливает, следует ли вставлять относительное положение абзаца, на который делается ссылка. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setNumberSeparator(String value)](#setNumberSeparator-java.lang.String-) | Задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setSuppressNonDelimiters(boolean value)](#setSuppressNonDelimiters-boolean-) | Устанавливает, подавлять ли символы, не являющиеся разделителями. |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | Выполняет развязку поля. |
| [update()](#update--) | Выполняет обновление поля. |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | Выполняет обновление поля. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### canWorkAsMergeField() {#canWorkAsMergeField--}
```
public boolean canWorkAsMergeField()
```




**Возвращает:**
логический
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


Получает имя закладки, на которую указывает ссылка.

**Возвращает:**
java.lang.String — имя указанной закладки.
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
### getIncludeNoteOrComment() {#getIncludeNoteOrComment--}
```
public boolean getIncludeNoteOrComment()
```


Определяет, следует ли увеличивать номера сносок, концевых сносок и аннотаций, отмеченных закладкой, и вставлять соответствующие сноски, концевые сноски и текст комментариев.

**Возвращает:**
boolean — следует ли увеличивать номера сносок, концевых сносок и аннотаций, отмеченных закладкой, и вставлять соответствующие сноски, концевые сноски и текст комментариев.
### getInsertHyperlink() {#getInsertHyperlink--}
```
public boolean getInsertHyperlink()
```


Получает, следует ли создавать гиперссылку на отмеченный закладкой абзац.

**Возвращает:**
boolean - Создавать ли гиперссылку на отмеченный абзац.
### getInsertParagraphNumber() {#getInsertParagraphNumber--}
```
public boolean getInsertParagraphNumber()
```


Получает, следует ли вставлять номер абзаца указанного абзаца точно так, как он отображается в документе.

**Возвращает:**
boolean — следует ли вставлять номер абзаца, на который указывает ссылка, точно так, как он отображается в документе.
### getInsertParagraphNumberInFullContext() {#getInsertParagraphNumberInFullContext--}
```
public boolean getInsertParagraphNumberInFullContext()
```


Определяет, следует ли вставлять номер абзаца указанного абзаца в полный контекст.

**Возвращает:**
boolean - Вставлять ли номер абзаца ссылочного абзаца в полный контекст.
### getInsertParagraphNumberInRelativeContext() {#getInsertParagraphNumberInRelativeContext--}
```
public boolean getInsertParagraphNumberInRelativeContext()
```


Определяет, вставлять ли номер абзаца ссылочного абзаца в относительный контекст.

**Возвращает:**
boolean — вставлять ли номер абзаца ссылочного абзаца в относительный контекст.
### getInsertRelativePosition() {#getInsertRelativePosition--}
```
public boolean getInsertRelativePosition()
```


Получает, следует ли вставить относительное положение абзаца, на который делается ссылка.

**Возвращает:**
boolean - Вставлять ли относительное положение абзаца, на который делается ссылка.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getMergeFieldName() {#getMergeFieldName--}
```
public String getMergeFieldName()
```




**Возвращает:**
java.lang.String
### getNumberSeparator() {#getNumberSeparator--}
```
public String getNumberSeparator()
```


Получает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

**Возвращает:**
java.lang.String — последовательность символов, используемая для разделения порядковых номеров и номеров страниц.
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
### getSuppressNonDelimiters() {#getSuppressNonDelimiters--}
```
public boolean getSuppressNonDelimiters()
```


Определяет, нужно ли подавлять символы, не являющиеся разделителями.

**Возвращает:**
boolean — подавлять ли символы, не являющиеся разделителями.
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

### isMergeValueRequired() {#isMergeValueRequired--}
```
public boolean isMergeValueRequired()
```




**Возвращает:**
логический
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


Устанавливает имя закладки, на которую указывает ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя указанной закладки. |

### setIncludeNoteOrComment(boolean value) {#setIncludeNoteOrComment-boolean-}
```
public void setIncludeNoteOrComment(boolean value)
```


Устанавливает, следует ли увеличивать сноску, концевую сноску и аннотацию, отмеченные закладкой, и вставлять соответствующую сноску, концевую сноску и текст комментария.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли увеличивать номера сносок, концевых сносок и аннотаций, отмеченных закладкой, и вставлять соответствующие сноски, концевые сноски и текст комментариев. |

### setInsertHyperlink(boolean value) {#setInsertHyperlink-boolean-}
```
public void setInsertHyperlink(boolean value)
```


Устанавливает, следует ли создавать гиперссылку на отмеченный закладкой абзац.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Создавать ли гиперссылку на отмеченный закладкой абзац. |

### setInsertParagraphNumber(boolean value) {#setInsertParagraphNumber-boolean-}
```
public void setInsertParagraphNumber(boolean value)
```


Устанавливает, следует ли вставлять номер абзаца ссылочного абзаца точно так, как он отображается в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли вставлять номер абзаца ссылочного абзаца точно так, как он отображается в документе. |

### setInsertParagraphNumberInFullContext(boolean value) {#setInsertParagraphNumberInFullContext-boolean-}
```
public void setInsertParagraphNumberInFullContext(boolean value)
```


Устанавливает, вставлять ли номер абзаца ссылочного абзаца в полный контекст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли номер абзаца ссылочного абзаца в полный контекст. |

### setInsertParagraphNumberInRelativeContext(boolean value) {#setInsertParagraphNumberInRelativeContext-boolean-}
```
public void setInsertParagraphNumberInRelativeContext(boolean value)
```


Устанавливает, вставлять ли номер абзаца ссылочного абзаца в относительный контекст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли номер абзаца ссылочного абзаца в относительный контекст. |

### setInsertRelativePosition(boolean value) {#setInsertRelativePosition-boolean-}
```
public void setInsertRelativePosition(boolean value)
```


Устанавливает, следует ли вставлять относительное положение абзаца, на который делается ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли относительное положение ссылочного абзаца. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setNumberSeparator(String value) {#setNumberSeparator-java.lang.String-}
```
public void setNumberSeparator(String value)
```


Задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, используемая для разделения порядковых номеров и номеров страниц. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setSuppressNonDelimiters(boolean value) {#setSuppressNonDelimiters-boolean-}
```
public void setSuppressNonDelimiters(boolean value)
```


Устанавливает, подавлять ли символы, не являющиеся разделителями.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли подавлять символы, не являющиеся разделителями. |

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
