---
title: FieldIndex
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле ИНДЕКС.
type: docs
weight: 206
url: /ru/java/com.aspose.words/fieldindex/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldIndex extends Field
```

Реализует поле ИНДЕКС.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Создает индекс, используя записи индекса, указанные в полях XE, и вставляет этот индекс в это место в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkName()](#getBookmarkName--) | Получает имя закладки, помечающей часть документа, используемую для построения индекса. |
| [getClass()](#getClass--) |  |
| [getCrossReferenceSeparator()](#getCrossReferenceSeparator--) | Получает последовательность символов, используемую для разделения перекрестных ссылок и других записей. |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getEntryType()](#getEntryType--) | Получает тип записи индекса, используемый для построения индекса. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getHeading()](#getHeading--) | Получает заголовок, который появляется в начале каждого набора записей для любой заданной буквы. |
| [getLanguageId()](#getLanguageId--) | Получает идентификатор языка, используемый для создания индекса. |
| [getLetterRange()](#getLetterRange--) | Получает диапазон букв, которым ограничивается индекс. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getNumberOfColumns()](#getNumberOfColumns--) | Получает количество столбцов на странице, используемых при построении индекса. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator--) | Получает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [getPageNumberSeparator()](#getPageNumberSeparator--) | Получает последовательность символов, которая используется для разделения записи указателя и ее номера страницы. |
| [getPageRangeSeparator()](#getPageRangeSeparator--) | Получает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getRunSubentriesOnSameLine()](#getRunSubentriesOnSameLine--) | Получает, запускаются ли подзаписи в той же строке, что и основная запись. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getSequenceName()](#getSequenceName--) | Получает имя последовательности, номер которой включен в номер страницы. |
| [getSequenceSeparator()](#getSequenceSeparator--) | Получает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [getUseYomi()](#getUseYomi--) | Определяет, следует ли разрешить использование текста йоми для записей указателя. |
| [hasPageNumberSeparator()](#hasPageNumberSeparator--) | Получает значение, указывающее, переопределяется ли разделитель номеров страниц кодом поля. |
| [hasSequenceName()](#hasSequenceName--) | Получает значение, указывающее, следует ли использовать последовательность при построении результатов поля. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Задает имя закладки, которая отмечает часть документа, используемую для построения индекса. |
| [setCrossReferenceSeparator(String value)](#setCrossReferenceSeparator-java.lang.String-) | Задает последовательность символов, используемую для разделения перекрестных ссылок и других записей. |
| [setEntryType(String value)](#setEntryType-java.lang.String-) | Задает тип записи индекса, используемый для построения индекса. |
| [setHeading(String value)](#setHeading-java.lang.String-) | Устанавливает заголовок, который появляется в начале каждого набора записей для любой заданной буквы. |
| [setLanguageId(String value)](#setLanguageId-java.lang.String-) | Задает идентификатор языка, используемый для создания индекса. |
| [setLetterRange(String value)](#setLetterRange-java.lang.String-) | Задает диапазон букв, которым ограничивается индекс. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setNumberOfColumns(String value)](#setNumberOfColumns-java.lang.String-) | Задает количество столбцов на странице, используемых при построении индекса. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String-) | Задает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [setPageNumberSeparator(String value)](#setPageNumberSeparator-java.lang.String-) | Задает последовательность символов, используемую для разделения записи указателя и ее номера страницы. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String-) | Задает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setRunSubentriesOnSameLine(boolean value)](#setRunSubentriesOnSameLine-boolean-) | Устанавливает, будут ли подзаголовки запускаться в той же строке, что и основная запись. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String-) | Задает имя последовательности, номер которой включен в номер страницы. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | Задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [setUseYomi(boolean value)](#setUseYomi-boolean-) | Устанавливает, следует ли разрешить использование текста йоми для записей указателя. |
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


Получает имя закладки, помечающей часть документа, используемую для построения индекса.

**Возвращает:**
java.lang.String — имя закладки, которая отмечает часть документа, используемую для построения индекса.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCrossReferenceSeparator() {#getCrossReferenceSeparator--}
```
public String getCrossReferenceSeparator()
```


Получает последовательность символов, используемую для разделения перекрестных ссылок и других записей.

**Возвращает:**
java.lang.String — последовательность символов, используемая для разделения перекрестных ссылок и других записей.
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


Получает тип записи индекса, используемый для построения индекса.

**Возвращает:**
java.lang.String — тип записи индекса, используемый для построения индекса.
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
### getHeading() {#getHeading--}
```
public String getHeading()
```


Получает заголовок, который появляется в начале каждого набора записей для любой заданной буквы.

**Возвращает:**
java.lang.String — заголовок, который появляется в начале каждого набора записей для любой заданной буквы.
### getLanguageId() {#getLanguageId--}
```
public String getLanguageId()
```


Получает идентификатор языка, используемый для создания индекса.

**Возвращает:**
java.lang.String — идентификатор языка, используемый для создания индекса.
### getLetterRange() {#getLetterRange--}
```
public String getLetterRange()
```


Получает диапазон букв, которым ограничивается индекс.

**Возвращает:**
java.lang.String — диапазон букв, которым ограничивается индекс.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getNumberOfColumns() {#getNumberOfColumns--}
```
public String getNumberOfColumns()
```


Получает количество столбцов на странице, используемых при построении индекса.

**Возвращает:**
java.lang.String — количество столбцов на странице, используемое при построении индекса.
### getPageNumberListSeparator() {#getPageNumberListSeparator--}
```
public String getPageNumberListSeparator()
```


Получает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц.

**Возвращает:**
java.lang.String — последовательность символов, используемая для разделения двух номеров страниц в списке номеров страниц.
### getPageNumberSeparator() {#getPageNumberSeparator--}
```
public String getPageNumberSeparator()
```


Получает последовательность символов, которая используется для разделения записи указателя и ее номера страницы.

**Возвращает:**
java.lang.String — последовательность символов, используемая для разделения записи указателя и номера ее страницы.
### getPageRangeSeparator() {#getPageRangeSeparator--}
```
public String getPageRangeSeparator()
```


Получает последовательность символов, используемую для разделения начала и конца диапазона страниц.

**Возвращает:**
java.lang.String — последовательность символов, используемая для разделения начала и конца диапазона страниц.
### getResult() {#getResult--}
```
public String getResult()
```


Получает текст, который находится между разделителем полей и концом поля.

**Возвращает:**
java.lang.String — текст между разделителем полей и концом поля.
### getRunSubentriesOnSameLine() {#getRunSubentriesOnSameLine--}
```
public boolean getRunSubentriesOnSameLine()
```


Получает, запускаются ли подзаписи в той же строке, что и основная запись.

**Возвращает:**
boolean - Выполнять ли подзаголовки в той же строке, что и основной ввод.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Получает узел, представляющий разделитель полей. Может быть нулевым.

**Возвращает:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - Узел, представляющий разделитель полей.
### getSequenceName() {#getSequenceName--}
```
public String getSequenceName()
```


Получает имя последовательности, номер которой включен в номер страницы.

**Возвращает:**
java.lang.String — имя последовательности, номер которой включен в номер страницы.
### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


Получает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

**Возвращает:**
java.lang.String — последовательность символов, используемая для разделения порядковых номеров и номеров страниц.
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
### getUseYomi() {#getUseYomi--}
```
public boolean getUseYomi()
```


Определяет, следует ли разрешить использование текста йоми для записей указателя.

**Возвращает:**
boolean — разрешить ли использование текста yomi для записей указателя.
### hasPageNumberSeparator() {#hasPageNumberSeparator--}
```
public boolean hasPageNumberSeparator()
```


Получает значение, указывающее, переопределяется ли разделитель номеров страниц кодом поля.

**Возвращает:**
boolean — значение, указывающее, переопределяется ли разделитель номеров страниц через код поля.
### hasSequenceName() {#hasSequenceName--}
```
public boolean hasSequenceName()
```


Получает значение, указывающее, следует ли использовать последовательность при построении результатов поля.

**Возвращает:**
boolean — значение, указывающее, следует ли использовать последовательность при построении результатов поля.
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


Задает имя закладки, которая отмечает часть документа, используемую для построения индекса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя закладки, помечающей часть документа, используемую для построения индекса. |

### setCrossReferenceSeparator(String value) {#setCrossReferenceSeparator-java.lang.String-}
```
public void setCrossReferenceSeparator(String value)
```


Задает последовательность символов, используемую для разделения перекрестных ссылок и других записей.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, используемая для разделения перекрестных ссылок и других записей. |

### setEntryType(String value) {#setEntryType-java.lang.String-}
```
public void setEntryType(String value)
```


Задает тип записи индекса, используемый для построения индекса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Тип записи индекса, используемый для построения индекса. |

### setHeading(String value) {#setHeading-java.lang.String-}
```
public void setHeading(String value)
```


Устанавливает заголовок, который появляется в начале каждого набора записей для любой заданной буквы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Заголовок, который появляется в начале каждого набора записей для любой данной буквы. |

### setLanguageId(String value) {#setLanguageId-java.lang.String-}
```
public void setLanguageId(String value)
```


Задает идентификатор языка, используемый для создания индекса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Идентификатор языка, используемый для создания индекса. |

### setLetterRange(String value) {#setLetterRange-java.lang.String-}
```
public void setLetterRange(String value)
```


Задает диапазон букв, которым ограничивается индекс.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Диапазон букв, которым ограничивается индекс. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setNumberOfColumns(String value) {#setNumberOfColumns-java.lang.String-}
```
public void setNumberOfColumns(String value)
```


Задает количество столбцов на странице, используемых при построении индекса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Количество столбцов на странице, используемое при построении индекса. |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String-}
```
public void setPageNumberListSeparator(String value)
```


Задает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, используемая для разделения двух номеров страниц в списке номеров страниц. |

### setPageNumberSeparator(String value) {#setPageNumberSeparator-java.lang.String-}
```
public void setPageNumberSeparator(String value)
```


Задает последовательность символов, используемую для разделения записи указателя и ее номера страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, используемая для разделения записи указателя и номера ее страницы. |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String-}
```
public void setPageRangeSeparator(String value)
```


Задает последовательность символов, используемую для разделения начала и конца диапазона страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, используемая для разделения начала и конца диапазона страниц. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setRunSubentriesOnSameLine(boolean value) {#setRunSubentriesOnSameLine-boolean-}
```
public void setRunSubentriesOnSameLine(boolean value)
```


Устанавливает, будут ли подзаголовки запускаться в той же строке, что и основная запись.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Выполнять ли подзаписи в той же строке, что и основную запись. |

### setSequenceName(String value) {#setSequenceName-java.lang.String-}
```
public void setSequenceName(String value)
```


Задает имя последовательности, номер которой включен в номер страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя последовательности, номер которой включен в номер страницы. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


Задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, используемая для разделения порядковых номеров и номеров страниц. |

### setUseYomi(boolean value) {#setUseYomi-boolean-}
```
public void setUseYomi(boolean value)
```


Устанавливает, следует ли разрешить использование текста йоми для записей указателя.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Включить ли использование текста йоми для записей указателя. |

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
