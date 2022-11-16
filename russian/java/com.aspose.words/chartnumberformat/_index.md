---
title: ChartNumberFormat
second_title: Справочник по API Aspose.Words для Java
description: Представляет числовое форматирование родительского элемента.
type: docs
weight: 67
url: /ru/java/com.aspose.words/chartnumberformat/
---

**Наследование:**
java.lang.Object
```
public class ChartNumberFormat
```

Представляет числовое форматирование родительского элемента.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getFormatCode()](#getFormatCode--) | Получает код формата, применяемый к метке данных. |
| [hashCode()](#hashCode--) |  |
| [isLinkedToSource()](#isLinkedToSource--) | Указывает, связан ли код формата с исходной ячейкой. |
| [isLinkedToSource(boolean value)](#isLinkedToSource-boolean-) | Указывает, связан ли код формата с исходной ячейкой. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFormatCode(String value)](#setFormatCode-java.lang.String-) | Задает код формата, применяемый к метке данных. |
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
### getFormatCode() {#getFormatCode--}
```
public String getFormatCode()
```


Получает код формата, применяемый к метке данных. Форматирование чисел используется для изменения способа отображения значения в метке данных и может использоваться очень творчески. Примеры числовых форматов:

Число - "\#,\#\#0.00"

Валюта - "\\"$\\"\#,\#\#0.00"

Время - "[$-x-systime]ч:мм:сс AM/PM"

Дата - "д/мм/гггг"

Процент - "0,00%"

Дробная часть - "\# ?/?"

Научный - "0.00E+00"

Текст - "@"

Бухгалтерия - "\_-\\"$\\"\ *\#,\#\#0.00\_-;-\\"$\\"\ *\#,\#\#0.00\_-;\_-\\"$\\"\ *\\"-\\"??\_-;\_-@\_-"

На заказ с цветом - "[Красный]-\#,\#\#0.0"

**Возвращает:**
java.lang.String — код формата, применяемый к метке данных.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isLinkedToSource() {#isLinkedToSource--}
```
public boolean isLinkedToSource()
```


Указывает, связан ли код формата с исходной ячейкой. Значение по умолчанию верно. NumberFormat будет сброшен на общий, если код формата связан с источником.

**Возвращает:**
boolean - соответствующее логическое значение.
### isLinkedToSource(boolean value) {#isLinkedToSource-boolean-}
```
public void isLinkedToSource(boolean value)
```


Указывает, связан ли код формата с исходной ячейкой. Значение по умолчанию верно. NumberFormat будет сброшен на общий, если код формата связан с источником.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setFormatCode(String value) {#setFormatCode-java.lang.String-}
```
public void setFormatCode(String value)
```


Задает код формата, применяемый к метке данных. Форматирование чисел используется для изменения способа отображения значения в метке данных и может использоваться очень творчески. Примеры числовых форматов:

Число - "\#,\#\#0.00"

Валюта - "\\"$\\"\#,\#\#0.00"

Время - "[$-x-systime]ч:мм:сс AM/PM"

Дата - "д/мм/гггг"

Процент - "0,00%"

Дробная часть - "\# ?/?"

Научный - "0.00E+00"

Текст - "@"

Бухгалтерия - "\_-\\"$\\"\ *\#,\#\#0.00\_-;-\\"$\\"\ *\#,\#\#0.00\_-;\_-\\"$\\"\ *\\"-\\"??\_-;\_-@\_-"

На заказ с цветом - "[Красный]-\#,\#\#0.0"

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Код формата, применяемый к метке данных. |

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
