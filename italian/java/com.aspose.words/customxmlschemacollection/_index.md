---
title: "CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words per Java"
description: "Una collezione di stringhe che rappresentano schemi XML associati a una parte XML personalizzata in Java."
type: docs
weight: 147
url: /it/java/com.aspose.words/customxmlschemacollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlSchemaCollection implements Iterable
```

Una raccolta di stringhe che rappresentano schemi XML associati a una parte XML personalizzata.

Per saperne di più, visita l'articolo di documentazione [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Non si creano istanze di questa classe. Si accede alla collezione di schemi XML di una parte XML personalizzata tramite la proprietà [CustomXmlPart.getSchemas()](../../com.aspose.words/customxmlpart/\#getSchemas).

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(String value)](#add-java.lang.String) | Aggiunge un elemento alla collezione. |
| [clear()](#clear) | Rimuove tutti gli elementi dalla raccolta. |
| [deepClone()](#deepClone) | Crea una copia profonda di questo oggetto. |
| [get(int index)](#get-int) | Ottiene l'elemento all'indice specificato. |
| [getCount()](#getCount) | Ottiene il numero di elementi contenuti nella collezione. |
| [indexOf(String value)](#indexOf-java.lang.String) | Restituisce l'indice basato su zero del valore specificato nella raccolta. |
| [iterator()](#iterator) | Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione. |
| [remove(String name)](#remove-java.lang.String) | Rimuove il valore specificato dalla raccolta. |
| [removeAt(int index)](#removeAt-int) | Rimuove un valore all'indice specificato. |
| [set(int index, String value)](#set-int-java.lang.String) | Imposta l'elemento all'indice specificato. |
### add(String value) {#add-java.lang.String}
```
public void add(String value)
```


Aggiunge un elemento alla collezione.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | L'elemento da aggiungere. |

### clear() {#clear}
```
public void clear()
```


Rimuove tutti gli elementi dalla raccolta.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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


Crea una copia profonda di questo oggetto.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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


Ottiene l'elemento all'indice specificato.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
java.lang.String - L'elemento all'indice specificato.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di elementi contenuti nella collezione.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
int - Il numero di elementi contenuti nella collezione.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Restituisce l'indice basato su zero del valore specificato nella raccolta.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore sensibile al maiuscolo/minuscolo da individuare. |

**Returns:**
int - L'indice basato su zero. Valore negativo se non trovato.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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


Rimuove il valore specificato dalla raccolta.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il valore sensibile al maiuscolo/minuscolo da rimuovere. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove un valore all'indice specificato.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Imposta l'elemento all'indice specificato.

 **Examples:** 

Mostra come lavorare con una collezione di schemi XML.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |
| valore | java.lang.String | L'elemento all'indice specificato. |

