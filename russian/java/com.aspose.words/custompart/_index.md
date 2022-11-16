---
title: CustomPart
second_title: Справочник по API Aspose.Words для Java
description: Представляет пользовательскую произвольную часть содержимого, которая не определена стандартом ISO/IEC 29500.
type: docs
weight: 102
url: /ru/java/com.aspose.words/custompart/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

Представляет пользовательскую часть (произвольное содержимое), которая не определена стандартом ISO/IEC 29500.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

Этот класс представляет часть OOXML, которая является целью "неизвестной связи". Все отношения, не определенные в ISO/IEC 29500, считаются «неизвестными отношениями». Неизвестные отношения разрешены в документе Office Open XML при условии, что они соответствуют рекомендациям по разметке отношений.

Microsoft Word сохраняет пользовательские части во время циклов открытия/сохранения. Некоторую дополнительную информацию можно найти здесь http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

 Aspose.Words также поддерживает пользовательские части и, кроме того, позволяет программно обращаться к таким частям через[CustomPart](../../com.aspose.words/custompart) а также[CustomPartCollection](../../com.aspose.words/custompartcollection) объекты.

 Не путайте пользовательские части с пользовательскими XML-данными. Использовать[CustomXmlPart](../../com.aspose.words/customxmlpart)если вам нужен доступ к пользовательским XML-данным.
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone--) | Делает «достаточно глубокую» копию объекта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getContentType()](#getContentType--) | Указывает тип содержимого этой пользовательской части. |
| [getData()](#getData--) | Содержит данные этой пользовательской детали. |
| [getName()](#getName--) | Получает абсолютное имя этой части в пакете OOXML или целевой URL-адрес. |
| [getRelationshipType()](#getRelationshipType--) | Получает тип отношения от родительской части к этой пользовательской части. |
| [hashCode()](#hashCode--) |  |
| [isExternal()](#isExternal--) | \{ False, если эта пользовательская часть хранится внутри пакета OOXML. |
| [isExternal(boolean value)](#isExternal-boolean-) | \{ False, если эта пользовательская часть хранится внутри пакета OOXML. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setContentType(String value)](#setContentType-java.lang.String-) | Указывает тип содержимого этой пользовательской части. |
| [setData(byte[] value)](#setData-byte---) | Содержит данные этой пользовательской детали. |
| [setName(String value)](#setName-java.lang.String-) | Задает абсолютное имя этой части в пакете OOXML или целевой URL. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String-) | Задает тип отношения от родительской части к этой пользовательской части. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public CustomPart deepClone()
```


 Делает «достаточно глубокую» копию объекта. Не дублирует байты[getData()](../../com.aspose.words/custompart\#getData--) / [setData(byte[])](../../com.aspose.words/custompart\#setData-byte---) ценность.

**Возвращает:**
[CustomPart](../../com.aspose.words/custompart)
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
### getContentType() {#getContentType--}
```
public String getContentType()
```


Указывает тип содержимого этой пользовательской части.

 Это свойство применимо только тогда, когда[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) является ложным.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getData() {#getData--}
```
public byte[] getData()
```


Содержит данные этой пользовательской детали.

 Это свойство применимо только тогда, когда[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) является ложным.

Значение по умолчанию — пустой массив байтов. Значение не может быть нулевым.

**Возвращает:**
байт[] - соответствующий байт[] ценность.
### getName() {#getName--}
```
public String getName()
```


Получает абсолютное имя этой части в пакете OOXML или целевой URL-адрес.

Если цель связи является внутренней, то это свойство является абсолютным именем части в пакете. Если цель отношения является внешней, то это свойство является целевым URL-адресом.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

**Возвращает:**
java.lang.String — абсолютное имя этой части в пакете OOXML или целевой URL.
### getRelationshipType() {#getRelationshipType--}
```
public String getRelationshipType()
```


Получает тип отношения от родительской части к этой пользовательской части.

Тип отношения для пользовательской детали должен быть «неизвестным», например, тип отношения пользователя, а не один из типов отношений, определенных в ISO/IEC 29500.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

**Возвращает:**
java.lang.String — тип отношения между родительской частью и этой настраиваемой частью.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isExternal() {#isExternal--}
```
public boolean isExternal()
```


\{ False, если эта пользовательская часть хранится внутри пакета OOXML. True, если эта настраиваемая часть является внешней целью.

Значение по умолчанию неверно .

**Возвращает:**
boolean - соответствующее логическое значение.
### isExternal(boolean value) {#isExternal-boolean-}
```
public void isExternal(boolean value)
```


\{ False, если эта пользовательская часть хранится внутри пакета OOXML. True, если эта настраиваемая часть является внешней целью.

Значение по умолчанию неверно .

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




### setContentType(String value) {#setContentType-java.lang.String-}
```
public void setContentType(String value)
```


Указывает тип содержимого этой пользовательской части.

 Это свойство применимо только тогда, когда[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) является ложным.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setData(byte[] value) {#setData-byte---}
```
public void setData(byte[] value)
```


Содержит данные этой пользовательской детали.

 Это свойство применимо только тогда, когда[isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) является ложным.

Значение по умолчанию — пустой массив байтов. Значение не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte[] | Соответствующий байт[] ценность. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Задает абсолютное имя этой части в пакете OOXML или целевой URL.

Если цель связи является внутренней, то это свойство является абсолютным именем части в пакете. Если цель отношения является внешней, то это свойство является целевым URL-адресом.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Абсолютное имя этой части в пакете OOXML или целевой URL. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String-}
```
public void setRelationshipType(String value)
```


Задает тип отношения от родительской части к этой пользовательской части.

Тип отношения для пользовательской детали должен быть «неизвестным», например, тип отношения пользователя, а не один из типов отношений, определенных в ISO/IEC 29500.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Тип связи между родительской деталью и этой настраиваемой деталью. |

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
