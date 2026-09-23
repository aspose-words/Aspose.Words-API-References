---
title: "CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words для Java"
description: "Коллекция строк, представляющих XML‑схемы, связанные с пользовательской частью XML в Java."
type: docs
weight: 147
url: /ru/java/com.aspose.words/customxmlschemacollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlSchemaCollection implements Iterable
```

Коллекция строк, представляющих XML‑схемы, связанные с пользовательской XML‑частью.

Чтобы узнать больше, посетите статью документации [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Вы не создаёте экземпляры этого класса. Вы получаете доступ к коллекции XML‑схем пользовательской части XML через свойство [CustomXmlPart.getSchemas()](../../com.aspose.words/customxmlpart/\#getSchemas).

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Методы

| Метод | Описание |
| --- | --- |
| [add(String value)](#add-java.lang.String) | Добавляет элемент в коллекцию. |
| [clear()](#clear) | Удаляет все элементы из коллекции. |
| [deepClone()](#deepClone) | Создаёт глубокую копию этого объекта. |
| [get(int index)](#get-int) | Получает элемент по указанному индексу. |
| [getCount()](#getCount) | Получает количество элементов, содержащихся в коллекции. |
| [indexOf(String value)](#indexOf-java.lang.String) | Возвращает индекс, начинающийся с нуля, указанного значения в коллекции. |
| [iterator()](#iterator) | Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции. |
| [remove(String name)](#remove-java.lang.String) | Удаляет указанное значение из коллекции. |
| [removeAt(int index)](#removeAt-int) | Удаляет значение по указанному индексу. |
| [set(int index, String value)](#set-int-java.lang.String) | Устанавливает элемент по указанному индексу. |
### add(String value) {#add-java.lang.String}
```
public void add(String value)
```


Добавляет элемент в коллекцию.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Элемент для добавления. |

### clear() {#clear}
```
public void clear()
```


Удаляет все элементы из коллекции.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

### deepClone() {#deepClone}
```
public CustomXmlSchemaCollection deepClone()
```


Создаёт глубокую копию этого объекта.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Returns:**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection/)
### get(int index) {#get-int}
```
public String get(int index)
```


Получает элемент по указанному индексу.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
java.lang.String - Элемент по указанному индексу.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество элементов, содержащихся в коллекции.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Returns:**
int — количество элементов, содержащихся в коллекции.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Возвращает индекс, начинающийся с нуля, указанного значения в коллекции.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Регистрозависимое значение для поиска. |

**Returns:**
int - Индекс, начинающийся с нуля. Отрицательное значение, если не найден.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Удаляет указанное значение из коллекции.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Регистрозависимое значение для удаления. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет значение по указанному индексу.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Устанавливает элемент по указанному индексу.

 **Examples:** 

Показывает, как работать с коллекцией XML‑схем.

```

 Document doc = new Document();

 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone the custom XML part's XML schema association collection,
 // and then add a couple of new schemas to the clone.
 CustomXmlSchemaCollection schemas = xmlPart.getSchemas().deepClone();
 schemas.add("http://www.w3.org/2001/XMLSchema-instance");
 schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

 Assert.assertEquals(3, schemas.getCount());
 Assert.assertEquals(2, schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

 // Enumerate the schemas and print each element.
 Iterator enumerator = schemas.iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next());
 }

 // Below are three ways of removing schemas from the collection.
 // 1 -  Remove a schema by index:
 schemas.removeAt(2);

 // 2 -  Remove a schema by value:
 schemas.remove("http://www.w3.org/2001/XMLSchema");

 // 3 -  Use the "Clear" method to empty the collection at once.
 schemas.clear();

 Assert.assertEquals(schemas.getCount(), 0);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |
| значение | java.lang.String | Элемент по указанному индексу. |

