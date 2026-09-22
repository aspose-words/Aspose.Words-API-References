---
title: "CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words لـ Java"
description: "مجموعة من السلاسل التي تمثل مخططات XML المرتبطة بجزء XML مخصص في Java."
type: docs
weight: 147
url: /ar/java/com.aspose.words/customxmlschemacollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlSchemaCollection implements Iterable
```

مجموعة من السلاسل التي تمثل مخططات XML المرتبطة بجزء XML مخصص.

لمزيد من المعلومات، زر مقالة الوثائق [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

لا تقوم بإنشاء كائنات من هذه الفئة. يمكنك الوصول إلى مجموعة مخططات XML لجزء XML مخصص عبر الخاصية [CustomXmlPart.getSchemas()](../../com.aspose.words/customxmlpart/\#getSchemas).

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(String value)](#add-java.lang.String) | يضيف عنصرًا إلى المجموعة. |
| [clear()](#clear) | يزيل جميع العناصر من المجموعة. |
| [deepClone()](#deepClone) | ينشئ نسخة عميقة من هذا الكائن. |
| [get(int index)](#get-int) | يحصل على العنصر في الفهرس المحدد. |
| [getCount()](#getCount) | يحصل على عدد العناصر الموجودة في المجموعة. |
| [indexOf(String value)](#indexOf-java.lang.String) | يعيد الفهرس الصفري للقيمة المحددة في المجموعة. |
| [iterator()](#iterator) | يعيد كائن مكرّر يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [remove(String name)](#remove-java.lang.String) | يزيل القيمة المحددة من المجموعة. |
| [removeAt(int index)](#removeAt-int) | يزيل قيمة عند الفهرس المحدد. |
| [set(int index, String value)](#set-int-java.lang.String) | يضبط العنصر في الفهرس المحدد. |
### add(String value) {#add-java.lang.String}
```
public void add(String value)
```


يضيف عنصرًا إلى المجموعة.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | العنصر المراد إضافته. |

### clear() {#clear}
```
public void clear()
```


يزيل جميع العناصر من المجموعة.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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


ينشئ نسخة عميقة من هذا الكائن.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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


يحصل على العنصر في الفهرس المحدد.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
java.lang.String - العنصر في الفهرس المحدد.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد العناصر الموجودة في المجموعة.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
int - عدد العناصر الموجودة في المجموعة.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


يعيد الفهرس الصفري للقيمة المحددة في المجموعة.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة حساسة لحالة الأحرف لتحديد الموقع. |

**Returns:**
int - الفهرس الصفري. قيمة سلبية إذا لم يتم العثور.
### iterator() {#iterator}
```
public Iterator iterator()
```


يعيد كائن مكرّر يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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


يزيل القيمة المحددة من المجموعة.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | القيمة حساسة لحالة الأحرف لإزالتها. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


يزيل قيمة عند الفهرس المحدد.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


يضبط العنصر في الفهرس المحدد.

 **Examples:** 

يوضح كيفية العمل مع مجموعة مخططات XML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |
| قيمة | java.lang.String | العنصر في الفهرس المحدد. |

