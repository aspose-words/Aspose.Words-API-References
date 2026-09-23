---
title: "OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words для Java"
description: "Представляет информацию об отдельной записи во внешнем источнике данных, которая должна быть исключена из слияния почты в Java."
type: docs
weight: 492
url: /ru/java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Представляет информацию о отдельной записи во внешнем источнике данных, которая должна быть исключена из слияния писем.

Чтобы узнать больше, посетите статью документации [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Если запись должна быть объединена в объединённый документ, то информация об этой записи не требуется. Однако, если данная запись не должна быть объединена в объединённый документ, то значение уникального ключа для этой записи должно быть сохранено в свойстве [getUniqueTag()](../../com.aspose.words/odsorecipientdata/#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/#setUniqueTag-byte) этого объекта, чтобы указать это исключение.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone) | Возвращает глубокую копию этого объекта. |
| [getActive()](#getActive) | Указывает, должна ли запись из источника данных быть импортирована в документ при выполнении слияния почты. |
| [getColumn()](#getColumn) | Указывает столбец в источнике данных, содержащий уникальные данные для текущей записи. |
| [getHash()](#getHash) | Представляет хеш‑код этой записи. |
| [getUniqueTag()](#getUniqueTag) | Указывает содержимое данной записи в столбце, содержащем уникальные данные. |
| [setActive(boolean value)](#setActive-boolean) | Указывает, должна ли запись из источника данных быть импортирована в документ при выполнении слияния почты. |
| [setColumn(int value)](#setColumn-int) | Указывает столбец в источнике данных, содержащий уникальные данные для текущей записи. |
| [setHash(int value)](#setHash-int) | Представляет хеш‑код этой записи. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | Указывает содержимое данной записи в столбце, содержащем уникальные данные. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


Возвращает глубокую копию этого объекта.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


Указывает, должна ли запись из источника данных быть импортирована в документ при выполнении слияния почты. Значение по умолчанию —  true .

**Returns:**
boolean - Соответствующее  boolean  значение.
### getColumn() {#getColumn}
```
public int getColumn()
```


Указывает столбец в источнике данных, содержащий уникальные данные для текущей записи. Значение по умолчанию — 0.

**Returns:**
int — соответствующее значение  int .
### getHash() {#getHash}
```
public int getHash()
```


Представляет хеш‑код этой записи. Иногда Microsoft Word использует [getHash()](../../com.aspose.words/odsorecipientdata/#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/#setHash-int) всей записи вместо значения [getUniqueTag()](../../com.aspose.words/odsorecipientdata/#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/#setUniqueTag-byte). Значение по умолчанию — 0.

**Returns:**
int — соответствующее значение  int .
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


Указывает содержимое данной записи в столбце, содержащем уникальные данные. Значение по умолчанию —  null .

**Returns:**
byte[] — соответствующее значение byte[].
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


Указывает, должна ли запись из источника данных быть импортирована в документ при выполнении слияния почты. Значение по умолчанию —  true .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Указывает столбец в источнике данных, содержащий уникальные данные для текущей записи. Значение по умолчанию — 0.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


Представляет хеш‑код этой записи. Иногда Microsoft Word использует [getHash()](../../com.aspose.words/odsorecipientdata/#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/#setHash-int) всей записи вместо значения [getUniqueTag()](../../com.aspose.words/odsorecipientdata/#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/#setUniqueTag-byte). Значение по умолчанию — 0.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


Указывает содержимое данной записи в столбце, содержащем уникальные данные. Значение по умолчанию —  null .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | byte[] | Соответствующее значение byte[]. |

