---
title: DocumentProperty
second_title: Справочник по API Aspose.Words для Java
description: Представляет пользовательское или встроенное свойство документа.
type: docs
weight: 126
url: /ru/java/com.aspose.words/documentproperty/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Представляет пользовательское или встроенное свойство документа.

 Чтобы узнать больше, посетите**Work with Document Properties** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getLinkSource()](#getLinkSource--) | Получает источник связанного пользовательского свойства документа. |
| [getName()](#getName--) | Возвращает имя свойства. |
| [getType()](#getType--) | Получает тип данных свойства. |
| [getValue()](#getValue--) | Получает значение свойства. |
| [hashCode()](#hashCode--) |  |
| [isLinkToContent()](#isLinkToContent--) | Показывает, связано ли это свойство с содержимым или нет. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setValue(Object value)](#setValue-java.lang.Object-) | Устанавливает значение свойства. |
| [toBool()](#toBool--) | Возвращает значение свойства как bool. |
| [toByteArray()](#toByteArray--) | Возвращает значение свойства в виде массива байтов. |
| [toDateTime()](#toDateTime--) | Возвращает значение свойства как DateTime в формате UTC. |
| [toDouble()](#toDouble--) | Возвращает значение свойства как двойное. |
| [toInt()](#toInt--) | Возвращает значение свойства как целое число. |
| [toString()](#toString--) | Возвращает значение свойства в виде строки, отформатированной в соответствии с текущей локалью. |
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
### getLinkSource() {#getLinkSource--}
```
public String getLinkSource()
```


Получает источник связанного пользовательского свойства документа.

**Возвращает:**
java.lang.String — источник связанного пользовательского свойства документа.
### getName() {#getName--}
```
public String getName()
```


Возвращает имя свойства.

Не может быть нулевым и не может быть пустой строкой.

**Возвращает:**
java.lang.String — имя свойства.
### getType() {#getType--}
```
public int getType()
```


Получает тип данных свойства.

**Возвращает:**
 int — тип данных свойства. Возвращаемое значение является одним из[PropertyType](../../com.aspose.words/propertytype) константы.
### getValue() {#getValue--}
```
public Object getValue()
```


Получает значение свойства.

Не может быть нулевым.

**Возвращает:**
java.lang.Object — значение свойства.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isLinkToContent() {#isLinkToContent--}
```
public boolean isLinkToContent()
```


Показывает, связано ли это свойство с содержимым или нет.

**Возвращает:**
boolean - соответствующее логическое значение.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setValue(Object value) {#setValue-java.lang.Object-}
```
public void setValue(Object value)
```


Устанавливает значение свойства.

Не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object | Стоимость имущества. |

### toBool() {#toBool--}
```
public boolean toBool()
```


Возвращает значение свойства как bool.

 Выдает исключение, если тип свойства не[PropertyType.BOOLEAN](../../com.aspose.words/propertytype\#BOOLEAN).

**Возвращает:**
логический
### toByteArray() {#toByteArray--}
```
public byte[] toByteArray()
```


Возвращает значение свойства в виде массива байтов.

 Выдает исключение, если тип свойства не[PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype\#BYTE-ARRAY).

**Возвращает:**
байт[]
### toDateTime() {#toDateTime--}
```
public Date toDateTime()
```


Возвращает значение свойства как DateTime в формате UTC.

 Выдает исключение, если тип свойства не[PropertyType.DATE\_TIME](../../com.aspose.words/propertytype\#DATE-TIME).

Microsoft Word хранит только часть даты (без времени) для настраиваемых свойств даты.

**Возвращает:**
java.util.Дата
### toDouble() {#toDouble--}
```
public double toDouble()
```


 Возвращает значение свойства как двойное. Выдает исключение, если тип свойства не[PropertyType.NUMBER](../../com.aspose.words/propertytype\#NUMBER).

**Возвращает:**
двойной
### toInt() {#toInt--}
```
public int toInt()
```


 Возвращает значение свойства как целое число. Выдает исключение, если тип свойства не[PropertyType.NUMBER](../../com.aspose.words/propertytype\#NUMBER).

**Возвращает:**
инт
### toString() {#toString--}
```
public String toString()
```


Возвращает значение свойства в виде строки, отформатированной в соответствии с текущей локалью.

Преобразует логическое свойство в "Y" или "N". Преобразует свойство даты в короткую строку даты. Для всех остальных типов свойство преобразуется с помощью Object.ToString().

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
