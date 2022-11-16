---
title: Revision
second_title: Справочник по API Aspose.Words для Java
description: Представляет отслеживаемое изменение в узле документа или стиле.
type: docs
weight: 483
url: /ru/java/com.aspose.words/revision/
---

**Наследование:**
java.lang.Object
```
public class Revision
```

Представляет редакцию (отслеживаемое изменение) в узле документа или стиле. Использовать[getRevisionType()](../../com.aspose.words/revision\#getRevisionType--) чтобы проверить тип этой ревизии.

 Чтобы узнать больше, посетите**Track Changes in a Document** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [accept()](#accept--) | Принимает эту версию. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAuthor()](#getAuthor--) | Получает автора этой версии. |
| [getClass()](#getClass--) |  |
| [getDateTime()](#getDateTime--) | Получает дату/время этой версии. |
| [getGroup()](#getGroup--) | Получает группу ревизий. |
| [getParentNode()](#getParentNode--) | Получает непосредственный родительский узел (владелец) этой ревизии. |
| [getParentStyle()](#getParentStyle--) | Получает непосредственный родительский стиль (владелец) этой ревизии. |
| [getRevisionType()](#getRevisionType--) | Получает тип этой редакции. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [reject()](#reject--) | Отклонить эту редакцию. |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | Устанавливает автора этой ревизии. |
| [setDateTime(Date value)](#setDateTime-java.util.Date-) | Устанавливает дату/время этой версии. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### accept() {#accept--}
```
public void accept()
```


Принимает эту версию.

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
### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


Получает автора этой версии. Не может быть пустой строкой или нулевым значением.

**Возвращает:**
java.lang.String — автор этой версии.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDateTime() {#getDateTime--}
```
public Date getDateTime()
```


Получает дату/время этой версии.

**Возвращает:**
java.util.Date — дата/время этой версии.
### getGroup() {#getGroup--}
```
public RevisionGroup getGroup()
```


Получает группу ревизий. Возвращает null, если ревизия не принадлежит ни к одной группе. Редакция не имеет группы, если тип редакции — RevisionType.StyleDefinitionChange или если редакция больше не существует в контексте документа (принята/отклонена).

**Возвращает:**
[RevisionGroup](../../com.aspose.words/revisiongroup) - Ревизионная группа.
### getParentNode() {#getParentNode--}
```
public Node getParentNode()
```


Получает непосредственный родительский узел (владелец) этой ревизии. Это свойство будет работать для любого типа ревизии, кроме[RevisionType.STYLE\_DEFINITION\_CHANGE](../../com.aspose.words/revisiontype\#STYLE-DEFINITION-CHANGE) . Если эта редакция связана с изменением форматирования стиля, используйте[getParentStyle()](../../com.aspose.words/revision\#getParentStyle--) вместо.

**Возвращает:**
[Node](../../com.aspose.words/node) - Непосредственный родительский узел (владелец) этой ревизии.
### getParentStyle() {#getParentStyle--}
```
public Style getParentStyle()
```


 Получает непосредственный родительский стиль (владелец) этой ревизии. Это свойство будет работать только для[RevisionType.STYLE\_DEFINITION\_CHANGE](../../com.aspose.words/revisiontype\#STYLE-DEFINITION-CHANGE) тип ревизии. Если эта редакция связана с изменениями в узлах документа, используйте[getParentNode()](../../com.aspose.words/revision\#getParentNode--) вместо.

**Возвращает:**
[Style](../../com.aspose.words/style) - Непосредственный родительский стиль (владелец) этой ревизии.
### getRevisionType() {#getRevisionType--}
```
public int getRevisionType()
```


Получает тип этой редакции.

**Возвращает:**
 int - Тип этой версии. Возвращаемое значение является одним из[RevisionType](../../com.aspose.words/revisiontype) константы.
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




### reject() {#reject--}
```
public void reject()
```


Отклонить эту редакцию.

### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


Устанавливает автора этой ревизии. Не может быть пустой строкой или нулевым значением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Автор этой редакции. |

### setDateTime(Date value) {#setDateTime-java.util.Date-}
```
public void setDateTime(Date value)
```


Устанавливает дату/время этой версии.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Дата/время этой редакции. |

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
