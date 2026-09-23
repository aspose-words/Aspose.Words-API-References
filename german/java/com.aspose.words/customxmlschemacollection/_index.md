---
title: "CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von Zeichenketten, die XML‑Schemas darstellen, die mit einem benutzerdefinierten XML‑Teil in Java verknüpft sind."
type: docs
weight: 147
url: /de/java/com.aspose.words/customxmlschemacollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlSchemaCollection implements Iterable
```

Eine Sammlung von Zeichenketten, die XML‑Schemata darstellen, die einem benutzerdefinierten XML‑Teil zugeordnet sind.

Weitere Informationen finden Sie im Dokumentationsartikel [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Sie erstellen keine Instanzen dieser Klasse. Sie greifen über die Eigenschaft [CustomXmlPart.getSchemas()](../../com.aspose.words/customxmlpart/\#getSchemas) auf die Sammlung von XML‑Schemas eines benutzerdefinierten XML‑Teils zu.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(String value)](#add-java.lang.String) | Fügt ein Element zur Sammlung hinzu. |
| [clear()](#clear) | Entfernt alle Elemente aus der Sammlung. |
| [deepClone()](#deepClone) | Erstellt eine tiefe Kopie dieses Objekts. |
| [get(int index)](#get-int) | Liest das Element am angegebenen Index. |
| [getCount()](#getCount) | Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente. |
| [indexOf(String value)](#indexOf-java.lang.String) | Gibt den nullbasierten Index des angegebenen Werts in der Sammlung zurück. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [remove(String name)](#remove-java.lang.String) | Entfernt den angegebenen Wert aus der Sammlung. |
| [removeAt(int index)](#removeAt-int) | Entfernt einen Wert am angegebenen Index. |
| [set(int index, String value)](#set-int-java.lang.String) | Setzt das Element am angegebenen Index. |
### add(String value) {#add-java.lang.String}
```
public void add(String value)
```


Fügt ein Element zur Sammlung hinzu.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Das hinzuzufügende Element. |

### clear() {#clear}
```
public void clear()
```


Entfernt alle Elemente aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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


Erstellt eine tiefe Kopie dieses Objekts.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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


Liest das Element am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
java.lang.String - Das Element am angegebenen Index.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
int – Die Anzahl der im Sammelobjekt enthaltenen Elemente.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Gibt den nullbasierten Index des angegebenen Werts in der Sammlung zurück.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der groß-/kleinschreibungssensible Wert zum Suchen. |

**Returns:**
int - Der nullbasierte Index. Negativer Wert, wenn nicht gefunden.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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


Entfernt den angegebenen Wert aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der groß-/kleinschreibungssensible Wert zum Entfernen. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt einen Wert am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Setzt das Element am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit einer XML‑Schema‑Sammlung arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |
| Wert | java.lang.String | Das Element am angegebenen Index. |

