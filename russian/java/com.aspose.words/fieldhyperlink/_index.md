---
title: FieldHyperlink
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле HYPERLINK
type: docs
weight: 199
url: /ru/java/com.aspose.words/fieldhyperlink/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldHyperlink extends Field
```

Реализует поле HYPERLINK

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Если выбрано, элемент управления переходит к местоположению, например к закладке или URL-адресу.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAddress()](#getAddress--) | Получает место, где эта гиперссылка переходит. |
| [getClass()](#getClass--) |  |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getOpenInNewWindow()](#getOpenInNewWindow--) | Получает, следует ли открывать целевой сайт в новом окне веб-браузера. |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getScreenTip()](#getScreenTip--) | Получает текст всплывающей подсказки для гиперссылки. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getSourceNode()](#getSourceNode--) |  |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSubAddress()](#getSubAddress--) | Получает место в файле, например закладку, куда переходит эта гиперссылка. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getTarget()](#getTarget--) | Получает цель, на которую должна быть перенаправлена ссылка. |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isImageMap()](#isImageMap--) | Определяет, следует ли добавлять координаты к гиперссылке для карты изображения на стороне сервера. |
| [isImageMap(boolean value)](#isImageMap-boolean-) | Устанавливает, следует ли добавлять координаты к гиперссылке для карты изображения на стороне сервера. |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setAddress(String value)](#setAddress-java.lang.String-) | Устанавливает место, где эта гиперссылка переходит. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setOpenInNewWindow(boolean value)](#setOpenInNewWindow-boolean-) | Устанавливает, открывать ли целевой сайт в новом окне веб-браузера. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setScreenTip(String value)](#setScreenTip-java.lang.String-) | Задает текст всплывающей подсказки для гиперссылки. |
| [setSubAddress(String value)](#setSubAddress-java.lang.String-) | Устанавливает место в файле, например закладку, куда переходит эта гиперссылка. |
| [setTarget(String value)](#setTarget-java.lang.String-) | Устанавливает цель, на которую должна быть перенаправлена ссылка. |
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
### getAddress() {#getAddress--}
```
public String getAddress()
```


Получает место, где эта гиперссылка переходит.

**Возвращает:**
java.lang.String — место перехода гиперссылки.
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
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getOpenInNewWindow() {#getOpenInNewWindow--}
```
public boolean getOpenInNewWindow()
```


Получает, следует ли открывать целевой сайт в новом окне веб-браузера.

**Возвращает:**
boolean — открывать ли целевой сайт в новом окне веб-браузера.
### getResult() {#getResult--}
```
public String getResult()
```


Получает текст, который находится между разделителем полей и концом поля.

**Возвращает:**
java.lang.String — текст между разделителем полей и концом поля.
### getScreenTip() {#getScreenTip--}
```
public String getScreenTip()
```


Получает текст всплывающей подсказки для гиперссылки.

**Возвращает:**
java.lang.String — Текст всплывающей подсказки для гиперссылки.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Получает узел, представляющий разделитель полей. Может быть нулевым.

**Возвращает:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - Узел, представляющий разделитель полей.
### getSourceNode() {#getSourceNode--}
```
public Inline getSourceNode()
```




**Возвращает:**
[Inline](../../com.aspose.words/inline)
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Получает узел, представляющий начало поля.

**Возвращает:**
[FieldStart](../../com.aspose.words/fieldstart) - Узел, представляющий начало поля.
### getSubAddress() {#getSubAddress--}
```
public String getSubAddress()
```


Получает место в файле, например закладку, куда переходит эта гиперссылка.

**Возвращает:**
java.lang.String — место в файле, например закладка, куда переходит эта гиперссылка.
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
### getTarget() {#getTarget--}
```
public String getTarget()
```


Получает цель, на которую должна быть перенаправлена ссылка.

**Возвращает:**
java.lang.String — цель, на которую должна быть перенаправлена ссылка.
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

### isImageMap() {#isImageMap--}
```
public boolean isImageMap()
```


Определяет, следует ли добавлять координаты к гиперссылке для карты изображения на стороне сервера.

**Возвращает:**
boolean — Добавлять ли координаты к гиперссылке для карты изображения на стороне сервера.
### isImageMap(boolean value) {#isImageMap-boolean-}
```
public void isImageMap(boolean value)
```


Устанавливает, следует ли добавлять координаты к гиперссылке для карты изображения на стороне сервера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Добавлять ли координаты к гиперссылке для карты изображения на стороне сервера. |

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
### setAddress(String value) {#setAddress-java.lang.String-}
```
public void setAddress(String value)
```


Устанавливает место, где эта гиперссылка переходит.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Место, где эта гиперссылка переходит. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setOpenInNewWindow(boolean value) {#setOpenInNewWindow-boolean-}
```
public void setOpenInNewWindow(boolean value)
```


Устанавливает, открывать ли целевой сайт в новом окне веб-браузера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Открывать ли целевой сайт в новом окне веб-браузера. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setScreenTip(String value) {#setScreenTip-java.lang.String-}
```
public void setScreenTip(String value)
```


Задает текст всплывающей подсказки для гиперссылки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст всплывающей подсказки для гиперссылки. |

### setSubAddress(String value) {#setSubAddress-java.lang.String-}
```
public void setSubAddress(String value)
```


Устанавливает место в файле, например закладку, куда переходит эта гиперссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Место в файле, например закладка, куда переходит эта гиперссылка. |

### setTarget(String value) {#setTarget-java.lang.String-}
```
public void setTarget(String value)
```


Устанавливает цель, на которую должна быть перенаправлена ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Цель, на которую должна быть перенаправлена ссылка. |

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
