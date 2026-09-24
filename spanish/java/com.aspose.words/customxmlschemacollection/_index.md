---
title: "CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de cadenas que representan esquemas XML asociados a una parte XML personalizada en Java."
type: docs
weight: 147
url: /es/java/com.aspose.words/customxmlschemacollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlSchemaCollection implements Iterable
```

Una colección de cadenas que representan esquemas XML asociados a una parte XML personalizada.

Para obtener más información, visite el artículo de documentación [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

No crea instancias de esta clase. Accede a la colección de esquemas XML de una parte XML personalizada mediante la propiedad [CustomXmlPart.getSchemas()](../../com.aspose.words/customxmlpart/\#getSchemas).

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(String value)](#add-java.lang.String) | Añade un elemento a la colección. |
| [clear()](#clear) | Elimina todos los elementos de la colección. |
| [deepClone()](#deepClone) | Crea una clonación profunda de este objeto. |
| [get(int index)](#get-int) | Obtiene el elemento en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
| [indexOf(String value)](#indexOf-java.lang.String) | Devuelve el índice basado en cero del valor especificado en la colección. |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [remove(String name)](#remove-java.lang.String) | Elimina el valor especificado de la colección. |
| [removeAt(int index)](#removeAt-int) | Elimina un valor en el índice especificado. |
| [set(int index, String value)](#set-int-java.lang.String) | Establece el elemento en el índice especificado. |
### add(String value) {#add-java.lang.String}
```
public void add(String value)
```


Añade un elemento a la colección.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El elemento a añadir. |

### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos de la colección.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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


Crea una clonación profunda de este objeto.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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


Obtiene el elemento en el índice especificado.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
java.lang.String - El elemento en el índice especificado.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
int - El número de elementos contenidos en la colección.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Devuelve el índice basado en cero del valor especificado en la colección.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor sensible a mayúsculas y minúsculas para localizar. |

**Returns:**
int - El índice basado en cero. Valor negativo si no se encuentra.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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


Elimina el valor especificado de la colección.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El valor sensible a mayúsculas y minúsculas para eliminar. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina un valor en el índice especificado.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Establece el elemento en el índice especificado.

 **Examples:** 

Muestra cómo trabajar con una colección de esquemas XML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |
| valor | java.lang.String | El elemento en el índice especificado. |

