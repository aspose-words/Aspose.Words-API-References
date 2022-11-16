---
title: OdsoRecipientData
second_title: Справочник по API Aspose.Words для Java
description: Представляет информацию об одной записи во внешнем источнике данных, которая должна быть исключена из слияния.
type: docs
weight: 416
url: /ru/java/com.aspose.words/odsorecipientdata/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Представляет информацию об одной записи во внешнем источнике данных, которая должна быть исключена из слияния.

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.

 Если запись должна быть объединена в объединенный документ, то никакой информации об этой записи не требуется. Однако, если данная запись не должна быть объединена в объединенный документ, то значение уникального ключа для этой записи должно храниться в[getUniqueTag()](../../com.aspose.words/odsorecipientdata\#getUniqueTag--) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata\#setUniqueTag-byte---) свойство этого объекта, чтобы указать это исключение.
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone--) | Возвращает глубокий клон этого объекта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getActive()](#getActive--) | Указывает, должна ли запись из источника данных импортироваться в документ при выполнении слияния. |
| [getClass()](#getClass--) |  |
| [getColumn()](#getColumn--) | Указывает столбец в источнике данных, который содержит уникальные данные для текущей записи. |
| [getHash()](#getHash--) | Представляет хэш-код для этой записи. |
| [getUniqueTag()](#getUniqueTag--) | Указывает содержимое данной записи в столбце, содержащем уникальные данные. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setActive(boolean value)](#setActive-boolean-) | Указывает, должна ли запись из источника данных импортироваться в документ при выполнении слияния. |
| [setColumn(int value)](#setColumn-int-) | Указывает столбец в источнике данных, который содержит уникальные данные для текущей записи. |
| [setHash(int value)](#setHash-int-) | Представляет хэш-код для этой записи. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte---) | Указывает содержимое данной записи в столбце, содержащем уникальные данные. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public OdsoRecipientData deepClone()
```


Возвращает глубокий клон этого объекта.

**Возвращает:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata)
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
### getActive() {#getActive--}
```
public boolean getActive()
```


Указывает, должна ли запись из источника данных импортироваться в документ при выполнении слияния. Значение по умолчанию верно .

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColumn() {#getColumn--}
```
public int getColumn()
```


Указывает столбец в источнике данных, который содержит уникальные данные для текущей записи. Значение по умолчанию — 0.

**Возвращает:**
int - соответствующее значение int.
### getHash() {#getHash--}
```
public int getHash()
```


 Представляет хэш-код для этой записи. Иногда Microsoft Word использует[getHash()](../../com.aspose.words/odsorecipientdata\#getHash--) / [setHash(int)](../../com.aspose.words/odsorecipientdata\#setHash-int-) целой записи вместо[getUniqueTag()](../../com.aspose.words/odsorecipientdata\#getUniqueTag--) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata\#setUniqueTag-byte---) ценность. Значение по умолчанию — 0.

**Возвращает:**
int - соответствующее значение int.
### getUniqueTag() {#getUniqueTag--}
```
public byte[] getUniqueTag()
```


Указывает содержимое данной записи в столбце, содержащем уникальные данные. Значение по умолчанию равно null .

**Возвращает:**
байт[] - соответствующий байт[] ценность.
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




### setActive(boolean value) {#setActive-boolean-}
```
public void setActive(boolean value)
```


Указывает, должна ли запись из источника данных импортироваться в документ при выполнении слияния. Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setColumn(int value) {#setColumn-int-}
```
public void setColumn(int value)
```


Указывает столбец в источнике данных, который содержит уникальные данные для текущей записи. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setHash(int value) {#setHash-int-}
```
public void setHash(int value)
```


 Представляет хэш-код для этой записи. Иногда Microsoft Word использует[getHash()](../../com.aspose.words/odsorecipientdata\#getHash--) / [setHash(int)](../../com.aspose.words/odsorecipientdata\#setHash-int-) целой записи вместо[getUniqueTag()](../../com.aspose.words/odsorecipientdata\#getUniqueTag--) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata\#setUniqueTag-byte---) ценность. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte---}
```
public void setUniqueTag(byte[] value)
```


Указывает содержимое данной записи в столбце, содержащем уникальные данные. Значение по умолчанию равно null .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte[] | Соответствующий байт[] ценность. |

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
