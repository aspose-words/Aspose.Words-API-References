---
title: XmlMapping
second_title: Справочник по API Aspose.Words для Java
description: Задает информацию, используемую для установления сопоставления между тегом родительского структурированного документа и элементом XML, хранящимся в пользовательской части данных XML в документе.
type: docs
weight: 629
url: /ru/java/com.aspose.words/xmlmapping/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class XmlMapping implements Cloneable
```

Задает информацию, используемую для установления сопоставления между тегом родительского структурированного документа и элементом XML, хранящимся в пользовательской части данных XML в документе.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [delete()](#delete--) | Удаляет сопоставление родительского структурированного документа с данными XML. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCustomXmlPart()](#getCustomXmlPart--) | Возвращает пользовательскую часть данных XML, с которой сопоставляется тег родительского структурированного документа. |
| [getPrefixMappings()](#getPrefixMappings--) |  Возвращает сопоставления префиксов пространств имен XML для оценки[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--). |
| [getStoreItemId()](#getStoreItemId--) |  Задает идентификатор пользовательских данных XML для пользовательской части данных XML, которая должна использоваться для оценки[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--) выражение. |
| [getXPath()](#getXPath--) | Возвращает выражение XPath, которое используется для поиска пользовательского узла XML, сопоставленного с тегом родительского структурированного документа. |
| [hashCode()](#hashCode--) |  |
| [isMapped()](#isMapped--) |  Возвращает**true** если тег родительского структурированного документа успешно сопоставлен с данными XML. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String-) | Задает сопоставление между тегом родительского структурированного документа и узлом XML пользовательской части данных XML. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### delete() {#delete--}
```
public void delete()
```


Удаляет сопоставление родительского структурированного документа с данными XML.

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
### getCustomXmlPart() {#getCustomXmlPart--}
```
public CustomXmlPart getCustomXmlPart()
```


Возвращает пользовательскую часть данных XML, с которой сопоставляется тег родительского структурированного документа.

**Возвращает:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - Пользовательская часть данных XML, с которой сопоставляется тег родительского структурированного документа.
### getPrefixMappings() {#getPrefixMappings--}
```
public String getPrefixMappings()
```


 Возвращает сопоставления префиксов пространств имен XML для оценки[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--). Указывает набор сопоставлений префиксов, которые должны использоваться для интерпретации выражения XPath, когда выражение XPath оценивается по сравнению с пользовательскими частями данных XML в документе.

**Возвращает:**
 java.lang.String — сопоставления префиксов пространств имен XML для оценки[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--).
### getStoreItemId() {#getStoreItemId--}
```
public String getStoreItemId()
```


 Задает идентификатор пользовательских данных XML для пользовательской части данных XML, которая должна использоваться для оценки[getXPath()](../../com.aspose.words/xmlmapping\#getXPath--) выражение.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getXPath() {#getXPath--}
```
public String getXPath()
```


Возвращает выражение XPath, которое используется для поиска пользовательского узла XML, сопоставленного с тегом родительского структурированного документа.

**Возвращает:**
java.lang.String — выражение XPath, которое используется для поиска пользовательского узла XML, сопоставленного с тегом родительского структурированного документа.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isMapped() {#isMapped--}
```
public boolean isMapped()
```


 Возвращает**true** если тег родительского структурированного документа успешно сопоставлен с данными XML.

**Возвращает:**
 логический -**true** если тег родительского структурированного документа успешно сопоставлен с данными XML.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String-}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


Задает сопоставление между тегом родительского структурированного документа и узлом XML пользовательской части данных XML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart) | Настраиваемая часть данных XML для сопоставления. |
| xPath | java.lang.String | Выражение XPath для поиска узла XML. |
| prefixMapping | java.lang.String | Сопоставления префиксов пространств имен XML для оценки XPath. |

**Возвращает:**
boolean — флаг, указывающий, успешно ли сопоставлен тег родительского структурированного документа с узлом XML.
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
