---
title: "CustomDocumentProperties"
linktitle: "CustomDocumentProperties"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung benutzerdefinierter Dokumenteigenschaften in Java."
type: docs
weight: 140
url: /de/java/com.aspose.words/customdocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class CustomDocumentProperties extends DocumentPropertyCollection
```

Eine Sammlung benutzerdefinierter Dokumenteigenschaften.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

Jedes [DocumentProperty](../../com.aspose.words/documentproperty/)‑Objekt stellt eine benutzerdefinierte Eigenschaft eines Containerdokuments dar.

Die Namen der Eigenschaften sind nicht zwischen Groß‑ und Kleinschreibung unterscheidend.

Die Eigenschaften in der Sammlung werden alphabetisch nach Namen sortiert.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.

```

 Document doc = new Document(getMyDir() + "Properties.docx");

 // Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
 // The document has a fixed list of built-in properties. The user creates all of the custom properties.
 Assert.assertEquals("Value of custom document property", doc.getCustomDocumentProperties().get("CustomProperty").toString());

 doc.getCustomDocumentProperties().add("CustomProperty2", "Value of custom document property #2");

 System.out.println("Custom Properties:");
 for (DocumentProperty customDocumentProperty : doc.getCustomDocumentProperties()) {
     System.out.println(customDocumentProperty.getName());
     System.out.println(MessageFormat.format("\tType:\t{0}", customDocumentProperty.getType()));
     System.out.println(MessageFormat.format("\tValue:\t\"{0}\"", customDocumentProperty.getValue()));
 }
 
```


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(String name, boolean value)](#add-java.lang.String-boolean) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN). |
| [add(String name, double value)](#add-java.lang.String-double) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.DOUBLE](../../com.aspose.words/propertytype/\#DOUBLE). |
| [add(String name, int value)](#add-java.lang.String-int) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER). |
| [add(String name, String value)](#add-java.lang.String-java.lang.String) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft. |
| [add(String name, Date value)](#add-java.lang.String-java.util.Date) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME). |
| [addLinkToContent(String name, String linkSource)](#addLinkToContent-java.lang.String-java.lang.String) | Erstellt eine neue, an den Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft. |
| [clear()](#clear) | Entfernt alle Eigenschaften aus der Sammlung. |
| [contains(String name)](#contains-java.lang.String) | Gibt  true  zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung existiert. |
| [get(int index)](#get-int) | Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/) Objekt nach Index zurück. |
| [get(String name)](#get-java.lang.String) | Stellt Zugriff auf die Elemente der Sammlung bereit. |
| [getCount()](#getCount) | Ermittelt die Anzahl der Elemente in der Sammlung. |
| [indexOf(String name)](#indexOf-java.lang.String) | Ermittelt den Index einer Eigenschaft anhand ihres Namens. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [remove(String name)](#remove-java.lang.String) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [removeAt(int index)](#removeAt-int) | Entfernt eine Eigenschaft am angegebenen Index. |
### add(String name, boolean value) {#add-java.lang.String-boolean}
```
public DocumentProperty add(String name, boolean value)
```


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN).

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Eigenschaft. |
| Wert | boolean | Der Wert der Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, double value) {#add-java.lang.String-double}
```
public DocumentProperty add(String name, double value)
```


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.DOUBLE](../../com.aspose.words/propertytype/\#DOUBLE).

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Eigenschaft. |
| Wert | double | Der Wert der Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, int value) {#add-java.lang.String-int}
```
public DocumentProperty add(String name, int value)
```


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER).

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Eigenschaft. |
| Wert | int | Der Wert der Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, String value) {#add-java.lang.String-java.lang.String}
```
public DocumentProperty add(String name, String value)
```


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft.  Erstellt eine neue benutzerdefinierte Dokumenteigenschaft vom Datentyp [PropertyType.STRING](../../com.aspose.words/propertytype/\#STRING).

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Eigenschaft. |
| Wert | java.lang.String | Der Wert der Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, Date value) {#add-java.lang.String-java.util.Date}
```
public DocumentProperty add(String name, Date value)
```


Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des Datentyps [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME).

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft erstellt, die ein Datum und eine Uhrzeit enthält.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Eigenschaft. |
| Wert | java.util.Date | Der Wert der Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### addLinkToContent(String name, String linkSource) {#addLinkToContent-java.lang.String-java.lang.String}
```
public DocumentProperty addLinkToContent(String name, String linkSource)
```


Erstellt eine neue, an den Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft mit einem Lesezeichen verknüpft.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("MyBookmark");
 builder.write("Hello world!");
 builder.endBookmark("MyBookmark");

 // Link a new custom property to a bookmark. The value of this property
 // will be the contents of the bookmark that it references in the "LinkSource" member.
 CustomDocumentProperties customProperties = doc.getCustomDocumentProperties();
 DocumentProperty customProperty = customProperties.addLinkToContent("Bookmark", "MyBookmark");

 Assert.assertEquals(true, customProperty.isLinkToContent());
 Assert.assertEquals("MyBookmark", customProperty.getLinkSource());
 Assert.assertEquals("Hello world!", customProperty.getValue());

 doc.save(getArtifactsDir() + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Eigenschaft. |
| linkSource | java.lang.String | Die Quelle der Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object or  null  when the  linkSource  is invalid.
### clear() {#clear}
```
public void clear()
```


Entfernt alle Eigenschaften aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Gibt  true  zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung existiert.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der Eigenschaft. |

**Returns:**
boolean -  true  wenn die Eigenschaft in der Sammlung existiert;  false  sonst.
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/) Objekt nach Index zurück.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.

```

 Document doc = new Document(getMyDir() + "Properties.docx");

 // Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
 // The document has a fixed list of built-in properties. The user creates all of the custom properties.
 Assert.assertEquals("Value of custom document property", doc.getCustomDocumentProperties().get("CustomProperty").toString());

 doc.getCustomDocumentProperties().add("CustomProperty2", "Value of custom document property #2");

 System.out.println("Custom Properties:");
 for (DocumentProperty customDocumentProperty : doc.getCustomDocumentProperties()) {
     System.out.println(customDocumentProperty.getName());
     System.out.println(MessageFormat.format("\tType:\t{0}", customDocumentProperty.getType()));
     System.out.println(MessageFormat.format("\tValue:\t\"{0}\"", customDocumentProperty.getValue()));
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int | Nullbasierter Index des zu holenden [DocumentProperty](../../com.aspose.words/documentproperty/). |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Stellt Zugriff auf die Elemente der Sammlung bereit.  Gibt ein [DocumentProperty](../../com.aspose.words/documentproperty/) Objekt anhand des Namens der Eigenschaft zurück.

 **Remarks:** 

Gibt  null  zurück, wenn keine Eigenschaft mit dem angegebenen Namen gefunden wird.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft erstellt, die ein Datum und eine Uhrzeit enthält.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der abzurufenden Eigenschaft. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der Elemente in der Sammlung.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.

```

 Document doc = new Document(getMyDir() + "Properties.docx");

 // Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
 // The document has a fixed list of built-in properties. The user creates all of the custom properties.
 Assert.assertEquals("Value of custom document property", doc.getCustomDocumentProperties().get("CustomProperty").toString());

 doc.getCustomDocumentProperties().add("CustomProperty2", "Value of custom document property #2");

 System.out.println("Custom Properties:");
 for (DocumentProperty customDocumentProperty : doc.getCustomDocumentProperties()) {
     System.out.println(customDocumentProperty.getName());
     System.out.println(MessageFormat.format("\tType:\t{0}", customDocumentProperty.getType()));
     System.out.println(MessageFormat.format("\tValue:\t\"{0}\"", customDocumentProperty.getValue()));
 }
 
```

**Returns:**
int - Anzahl der Elemente in der Sammlung.
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Ermittelt den Index einer Eigenschaft anhand ihres Namens.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der Eigenschaft. |

**Returns:**
int - Der nullbasierte Index. Negativer Wert, wenn nicht gefunden.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht‑groß-/kleinschreibungssensible Name der Eigenschaft. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt eine Eigenschaft am angegebenen Index.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index. |

