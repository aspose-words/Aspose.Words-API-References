---
title: FieldDde
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле DDE.
type: docs
weight: 178
url: /ru/java/com.aspose.words/fielddde/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldDde extends Field
```

Реализует поле DDE.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Для информации, скопированной из другого приложения, это поле связывает эту информацию с исходным исходным файлом с помощью DDE.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAutoUpdate()](#getAutoUpdate--) | Получает, следует ли обновлять это поле автоматически. |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getInsertAsBitmap()](#getInsertAsBitmap--) | Определяет, следует ли вставлять связанный объект в виде растрового изображения. |
| [getInsertAsHtml()](#getInsertAsHtml--) | Определяет, вставлять ли связанный объект как текст в формате HTML. |
| [getInsertAsPicture()](#getInsertAsPicture--) | Определяет, следует ли вставлять связанный объект в виде изображения. |
| [getInsertAsRtf()](#getInsertAsRtf--) | Определяет, следует ли вставлять связанный объект в формате RTF. |
| [getInsertAsText()](#getInsertAsText--) | Получает, следует ли вставлять связанный объект в текстовом формате. |
| [getInsertAsUnicode()](#getInsertAsUnicode--) | Получает, следует ли вставлять связанный объект как текст Unicode. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getProgId()](#getProgId--) | Получает тип приложения информации о ссылке. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getSourceFullName()](#getSourceFullName--) | Получает имя и расположение исходного файла. |
| [getSourceItem()](#getSourceItem--) | Получает часть исходного файла, которая связывается. |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isLinked()](#isLinked--) | Определяет, следует ли уменьшить размер файла, не сохраняя графические данные вместе с документом. |
| [isLinked(boolean value)](#isLinked-boolean-) | Устанавливает, следует ли уменьшать размер файла, не сохраняя графические данные вместе с документом. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean-) | Устанавливает, обновлять ли это поле автоматически. |
| [setInsertAsBitmap(boolean value)](#setInsertAsBitmap-boolean-) | Устанавливает, следует ли вставлять связанный объект в виде растрового изображения. |
| [setInsertAsHtml(boolean value)](#setInsertAsHtml-boolean-) | Устанавливает, следует ли вставлять связанный объект как текст в формате HTML. |
| [setInsertAsPicture(boolean value)](#setInsertAsPicture-boolean-) | Устанавливает, следует ли вставлять связанный объект в виде изображения. |
| [setInsertAsRtf(boolean value)](#setInsertAsRtf-boolean-) | Устанавливает, следует ли вставлять связанный объект в формате расширенного текста (RTF). |
| [setInsertAsText(boolean value)](#setInsertAsText-boolean-) | Устанавливает, следует ли вставлять связанный объект в текстовом формате. |
| [setInsertAsUnicode(boolean value)](#setInsertAsUnicode-boolean-) | Устанавливает, следует ли вставлять связанный объект как текст Unicode. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setProgId(String value)](#setProgId-java.lang.String-) | Задает тип приложения информации о ссылке. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | Задает имя и расположение исходного файла. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String-) | Задает связываемую часть исходного файла. |
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
### getAutoUpdate() {#getAutoUpdate--}
```
public boolean getAutoUpdate()
```


Получает, следует ли обновлять это поле автоматически.

**Возвращает:**
boolean - Обновлять ли это поле автоматически.
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
### getInsertAsBitmap() {#getInsertAsBitmap--}
```
public boolean getInsertAsBitmap()
```


Определяет, следует ли вставлять связанный объект в виде растрового изображения.

**Возвращает:**
boolean — следует ли вставлять связанный объект в виде растрового изображения.
### getInsertAsHtml() {#getInsertAsHtml--}
```
public boolean getInsertAsHtml()
```


Определяет, вставлять ли связанный объект как текст в формате HTML.

**Возвращает:**
boolean — следует ли вставлять связанный объект как текст в формате HTML.
### getInsertAsPicture() {#getInsertAsPicture--}
```
public boolean getInsertAsPicture()
```


Определяет, следует ли вставлять связанный объект в виде изображения.

**Возвращает:**
boolean - Вставлять ли связанный объект в виде изображения.
### getInsertAsRtf() {#getInsertAsRtf--}
```
public boolean getInsertAsRtf()
```


Определяет, следует ли вставлять связанный объект в формате RTF.

**Возвращает:**
boolean — следует ли вставлять связанный объект в формате RTF.
### getInsertAsText() {#getInsertAsText--}
```
public boolean getInsertAsText()
```


Получает, следует ли вставлять связанный объект в текстовом формате.

**Возвращает:**
boolean — следует ли вставлять связанный объект в текстовом формате.
### getInsertAsUnicode() {#getInsertAsUnicode--}
```
public boolean getInsertAsUnicode()
```


Получает, следует ли вставлять связанный объект как текст Unicode.

**Возвращает:**
boolean — следует ли вставлять связанный объект как текст Unicode.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getProgId() {#getProgId--}
```
public String getProgId()
```


Получает тип приложения информации о ссылке.

**Возвращает:**
java.lang.String — Тип приложения информации о ссылке.
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
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


Получает имя и расположение исходного файла.

**Возвращает:**
java.lang.String — имя и расположение исходного файла.
### getSourceItem() {#getSourceItem--}
```
public String getSourceItem()
```


Получает часть исходного файла, которая связывается.

**Возвращает:**
java.lang.String — часть исходного файла, на которую делается ссылка.
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

### isLinked() {#isLinked--}
```
public boolean isLinked()
```


Определяет, следует ли уменьшить размер файла, не сохраняя графические данные вместе с документом.

**Возвращает:**
boolean — следует ли уменьшать размер файла, не сохраняя графические данные вместе с документом.
### isLinked(boolean value) {#isLinked-boolean-}
```
public void isLinked(boolean value)
```


Устанавливает, следует ли уменьшать размер файла, не сохраняя графические данные вместе с документом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Уменьшать ли размер файла, не сохраняя графические данные вместе с документом. |

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
### setAutoUpdate(boolean value) {#setAutoUpdate-boolean-}
```
public void setAutoUpdate(boolean value)
```


Устанавливает, обновлять ли это поле автоматически.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Обновлять ли это поле автоматически. |

### setInsertAsBitmap(boolean value) {#setInsertAsBitmap-boolean-}
```
public void setInsertAsBitmap(boolean value)
```


Устанавливает, следует ли вставлять связанный объект в виде растрового изображения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли связанный объект в виде растрового изображения. |

### setInsertAsHtml(boolean value) {#setInsertAsHtml-boolean-}
```
public void setInsertAsHtml(boolean value)
```


Устанавливает, следует ли вставлять связанный объект как текст в формате HTML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли связанный объект как текст в формате HTML. |

### setInsertAsPicture(boolean value) {#setInsertAsPicture-boolean-}
```
public void setInsertAsPicture(boolean value)
```


Устанавливает, следует ли вставлять связанный объект в виде изображения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли связанный объект в виде изображения. |

### setInsertAsRtf(boolean value) {#setInsertAsRtf-boolean-}
```
public void setInsertAsRtf(boolean value)
```


Устанавливает, следует ли вставлять связанный объект в формате расширенного текста (RTF).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли вставлять связанный объект в формате RTF. |

### setInsertAsText(boolean value) {#setInsertAsText-boolean-}
```
public void setInsertAsText(boolean value)
```


Устанавливает, следует ли вставлять связанный объект в текстовом формате.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли связанный объект в текстовом формате. |

### setInsertAsUnicode(boolean value) {#setInsertAsUnicode-boolean-}
```
public void setInsertAsUnicode(boolean value)
```


Устанавливает, следует ли вставлять связанный объект как текст Unicode.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вставлять ли связанный объект как текст Unicode. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setProgId(String value) {#setProgId-java.lang.String-}
```
public void setProgId(String value)
```


Задает тип приложения информации о ссылке.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Тип приложения информации о ссылке. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


Задает имя и расположение исходного файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя и расположение исходного файла. |

### setSourceItem(String value) {#setSourceItem-java.lang.String-}
```
public void setSourceItem(String value)
```


Задает связываемую часть исходного файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Связываемая часть исходного файла. |

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
