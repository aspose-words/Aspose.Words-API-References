---
title: CustomXmlPart
second_title: Справочник по API Aspose.Words для Java
description: Представляет пользовательские XML-данные пользовательской части хранилища данных XML в пакете.
type: docs
weight: 104
url: /ru/java/com.aspose.words/customxmlpart/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class CustomXmlPart implements Cloneable
```

Представляет часть хранилища пользовательских данных XML (пользовательские данные XML в пакете).

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

 Документ DOCX или DOC может содержать одну или несколько частей Custom XML Data Storage. Aspose.Words сохраняет и позволяет создавать и извлекать пользовательские XML-данные через[Document.getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) коллекция.
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone--) | Делает «достаточно глубокую» копию объекта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getData()](#getData--) | Получает XML-содержимое этой пользовательской части хранилища данных XML. |
| [getDataChecksum()](#getDataChecksum--) |  Указывает контрольную сумму циклическим избыточным кодом (CRC)[getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---) содержание. |
| [getId()](#getId--) | Получает строку, идентифицирующую эту пользовательскую часть XML в документе OOXML. |
| [getSchemas()](#getSchemas--) | Указывает набор схем XML, связанных с этой настраиваемой частью XML. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setData(byte[] value)](#setData-byte---) | Задает XML-содержимое этой пользовательской части хранения данных XML. |
| [setId(String value)](#setId-java.lang.String-) | Задает строку, идентифицирующую эту пользовательскую часть XML в документе OOXML. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public CustomXmlPart deepClone()
```


 Делает «достаточно глубокую» копию объекта. Не дублирует байты[getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---) ценность.

**Возвращает:**
[CustomXmlPart](../../com.aspose.words/customxmlpart)
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
### getData() {#getData--}
```
public byte[] getData()
```


Получает XML-содержимое этой пользовательской части хранилища данных XML.

Значение по умолчанию — пустой массив байтов. Значение не может быть нулевым.

**Возвращает:**
байт[— XML-содержимое этой пользовательской части хранилища данных XML.
### getDataChecksum() {#getDataChecksum--}
```
public long getDataChecksum()
```


 Указывает контрольную сумму циклическим избыточным кодом (CRC)[getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---) содержание.

**Возвращает:**
long — соответствующее длинное значение.
### getId() {#getId--}
```
public String getId()
```


Получает строку, идентифицирующую эту пользовательскую часть XML в документе OOXML.

ISO/IEC 29500 указывает, что это значение является идентификатором GUID, но старые версии Microsoft Word допускали здесь любую строку. Aspose.Words делает то же самое для формата ECMA-376. Но обратите внимание, что Microsoft Word Online не может открыть документ, созданный со значением, отличным от GUID. Таким образом, GUID является предпочтительным значением для этого свойства.

Допустимое значение должно быть идентификатором, уникальным среди всех пользовательских частей XML-данных в этом документе.

Значение по умолчанию — пустая строка. Значение не может быть нулевым.

**Возвращает:**
java.lang.String — строка, идентифицирующая эту пользовательскую часть XML в документе OOXML.
### getSchemas() {#getSchemas--}
```
public CustomXmlSchemaCollection getSchemas()
```


Указывает набор схем XML, связанных с этой настраиваемой частью XML.

**Возвращает:**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection) - соответствующий[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection) ценность.
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




### setData(byte[] value) {#setData-byte---}
```
public void setData(byte[] value)
```


Задает XML-содержимое этой пользовательской части хранения данных XML.

Значение по умолчанию — пустой массив байтов. Значение не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte[] | XML-содержимое этой пользовательской части хранилища данных XML. |

### setId(String value) {#setId-java.lang.String-}
```
public void setId(String value)
```


Задает строку, идентифицирующую эту пользовательскую часть XML в документе OOXML.

ISO/IEC 29500 указывает, что это значение является идентификатором GUID, но старые версии Microsoft Word допускали здесь любую строку. Aspose.Words делает то же самое для формата ECMA-376. Но обратите внимание, что Microsoft Word Online не может открыть документ, созданный со значением, отличным от GUID. Таким образом, GUID является предпочтительным значением для этого свойства.

Допустимое значение должно быть идентификатором, уникальным среди всех пользовательских частей XML-данных в этом документе.

Значение по умолчанию — пустая строка. Значение не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Строка, идентифицирующая эту пользовательскую часть XML в документе OOXML. |

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
