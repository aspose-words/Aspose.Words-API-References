---
title: "CustomPart"
linktitle: "CustomPart"
second_title: "Aspose.Words для Java"
description: "Представляет пользовательскую произвольную часть содержимого, которая не определена стандартом ISO/IEC 29500 в Java."
type: docs
weight: 141
url: /ru/java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

Представляет пользовательскую (произвольного содержания) часть, которая не определена стандартом ISO/IEC 29500.

Чтобы узнать больше, посетите статью документации [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Этот класс представляет часть OOXML, являющуюся целью «неизвестного отношения». Все отношения, не определённые в ISO/IEC 29500, считаются «неизвестными отношениями». Неизвестные отношения допускаются в документе Office Open XML при условии соответствия рекомендациям по разметке отношений.

Microsoft Word сохраняет пользовательские части во время циклов открытия/сохранения. Дополнительную информацию можно найти здесь http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words также поддерживает передачу пользовательских частей и, кроме того, позволяет программно получать доступ к таким частям через объекты [CustomPart](../../com.aspose.words/custompart/) и [CustomPartCollection](../../com.aspose.words/custompartcollection/).

Не путайте пользовательские части с данными Custom XML. Используйте [CustomXmlPart](../../com.aspose.words/customxmlpart/), если необходимо получить доступ к данным Custom XML.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone) | Создаёт «достаточно глубокую» копию объекта. |
| [getContentType()](#getContentType) | Указывает тип содержимого этой пользовательской части. |
| [getData()](#getData) | Содержит данные этой пользовательской части. |
| [getName()](#getName) | Получает абсолютное имя этой части внутри пакета OOXML или целевой URL. |
| [getRelationshipType()](#getRelationshipType) | Получает тип отношения от родительской части к этой пользовательской части. |
| [isExternal()](#isExternal) | Ложно, если эта пользовательская часть хранится внутри пакета OOXML. |
| [isExternal(boolean value)](#isExternal-boolean) | Ложно, если эта пользовательская часть хранится внутри пакета OOXML. |
| [setContentType(String value)](#setContentType-java.lang.String) | Указывает тип содержимого этой пользовательской части. |
| [setData(byte[] value)](#setData-byte) | Содержит данные этой пользовательской части. |
| [setName(String value)](#setName-java.lang.String) | Устанавливает абсолютное имя этой части внутри пакета OOXML или целевой URL. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String) | Устанавливает тип отношения от родительской части к этой пользовательской части. |
### deepClone() {#deepClone}
```
public CustomPart deepClone()
```


Создаёт «достаточно глубокую» копию объекта. Не дублирует байты значения [getData()](../../com.aspose.words/custompart/\#getData) / [setData(byte[])](../../com.aspose.words/custompart/\#setData-byte).

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
[CustomPart](../../com.aspose.words/custompart/)
### getContentType() {#getContentType}
```
public String getContentType()
```


Указывает тип содержимого этой пользовательской части.

 **Remarks:** 

Это свойство применимо только когда [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) равно false.

Значение по умолчанию — пустая строка. Действительное значение должно быть непустой строкой.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getData() {#getData}
```
public byte[] getData()
```


Содержит данные этой пользовательской части.

 **Remarks:** 

Это свойство применимо только когда [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) равно false.

Значение по умолчанию — пустой массив байтов. Значение не может быть null.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
byte[] — соответствующее значение byte[].
### getName() {#getName}
```
public String getName()
```


Получает абсолютное имя этой части внутри пакета OOXML или целевой URL.

 **Remarks:** 

Если цель отношения внутренняя, то это свойство представляет собой абсолютное имя части внутри пакета. Если цель отношения внешняя, то это свойство представляет собой целевой URL.

Значение по умолчанию — пустая строка. Действительное значение должно быть непустой строкой.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String — абсолютное имя этой части внутри пакета OOXML или целевой URL.
### getRelationshipType() {#getRelationshipType}
```
public String getRelationshipType()
```


Получает тип отношения от родительской части к этой пользовательской части.

 **Remarks:** 

Тип отношения для пользовательской части должен быть «unknown», например пользовательский тип отношения, а не один из типов отношений, определённых в ISO/IEC 29500.

Значение по умолчанию — пустая строка. Действительное значение должно быть непустой строкой.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String — тип отношения от родительской части к этой пользовательской части.
### isExternal() {#isExternal}
```
public boolean isExternal()
```


Ложно, если эта пользовательская часть хранится внутри пакета OOXML. Истинно, если эта пользовательская часть является внешней целью.

 **Remarks:** 

Значение по умолчанию — false.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### isExternal(boolean value) {#isExternal-boolean}
```
public void isExternal(boolean value)
```


Ложно, если эта пользовательская часть хранится внутри пакета OOXML. Истинно, если эта пользовательская часть является внешней целью.

 **Remarks:** 

Значение по умолчанию — false.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Указывает тип содержимого этой пользовательской части.

 **Remarks:** 

Это свойство применимо только когда [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) равно false.

Значение по умолчанию — пустая строка. Действительное значение должно быть непустой строкой.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Содержит данные этой пользовательской части.

 **Remarks:** 

Это свойство применимо только когда [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) равно false.

Значение по умолчанию — пустой массив байтов. Значение не может быть null.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | byte[] | Соответствующее значение byte[]. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Устанавливает абсолютное имя этой части внутри пакета OOXML или целевой URL.

 **Remarks:** 

Если цель отношения внутренняя, то это свойство представляет собой абсолютное имя части внутри пакета. Если цель отношения внешняя, то это свойство представляет собой целевой URL.

Значение по умолчанию — пустая строка. Действительное значение должно быть непустой строкой.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Абсолютное имя этой части внутри пакета OOXML или целевой URL. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String}
```
public void setRelationshipType(String value)
```


Устанавливает тип отношения от родительской части к этой пользовательской части.

 **Remarks:** 

Тип отношения для пользовательской части должен быть «unknown», например пользовательский тип отношения, а не один из типов отношений, определённых в ISO/IEC 29500.

Значение по умолчанию — пустая строка. Действительное значение должно быть непустой строкой.

 **Examples:** 

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Тип отношения от родительской части к этой пользовательской части. |

