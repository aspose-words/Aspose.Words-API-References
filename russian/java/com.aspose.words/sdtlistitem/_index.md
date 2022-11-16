---
title: SdtListItem
second_title: Справочник по API Aspose.Words для Java
description: Этот элемент указывает один элемент списка в родительском или структурированном теге документа.
type: docs
weight: 506
url: /ru/java/com.aspose.words/sdtlistitem/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class SdtListItem implements Cloneable
```

 Этот элемент определяет один элемент списка в родительском элементе.[SdtType.COMBO\_BOX](../../com.aspose.words/sdttype\#COMBO-BOX) или же[SdtType.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype\#DROP-DOWN-LIST) тег структурированного документа.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [SdtListItem(String displayText, String value)](#SdtListItem-java.lang.String-java.lang.String-) | Инициализирует новый экземпляр этого класса. |
| [SdtListItem(String value)](#SdtListItem-java.lang.String-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayText()](#getDisplayText--) |  Получает текст для отображения в содержимом выполнения вместо[getValue()](../../com.aspose.words/sdtlistitem\#getValue--) содержимое атрибута для этого элемента списка. |
| [getValue()](#getValue--) | Получает значение этого элемента списка. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### SdtListItem(String displayText, String value) {#SdtListItem-java.lang.String-java.lang.String-}
```
public SdtListItem(String displayText, String value)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| displayText | java.lang.String |  |
| value | java.lang.String |  |

### SdtListItem(String value) {#SdtListItem-java.lang.String-}
```
public SdtListItem(String value)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  |

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
### getDisplayText() {#getDisplayText--}
```
public String getDisplayText()
```


 Получает текст для отображения в содержимом выполнения вместо[getValue()](../../com.aspose.words/sdtlistitem\#getValue--) содержимое атрибута для этого элемента списка.

Не может быть нулевым и не может быть пустой строкой.

**Возвращает:**
 java.lang.String — текст, отображаемый в содержимом запуска вместо[getValue()](../../com.aspose.words/sdtlistitem\#getValue--) содержимое атрибута для этого элемента списка.
### getValue() {#getValue--}
```
public String getValue()
```


Получает значение этого элемента списка.

Не может быть нулевым и не может быть пустой строкой.

**Возвращает:**
java.lang.String — значение этого элемента списка.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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
