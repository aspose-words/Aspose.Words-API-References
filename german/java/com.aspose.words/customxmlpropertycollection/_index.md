---
title: "CustomXmlPropertyCollection"
linktitle: "CustomXmlPropertyCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von benutzerdefinierten XML-Attributen oder Smart-Tag-Eigenschaften in Java dar."
type: docs
weight: 146
url: /de/java/com.aspose.words/customxmlpropertycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlPropertyCollection implements Iterable
```

Stellt eine Sammlung von benutzerdefinierten XML‑Attributen oder Smart‑Tag‑Eigenschaften dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Elemente sind [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) Objekte.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(CustomXmlProperty property)](#add-com.aspose.words.CustomXmlProperty) | Fügt der Sammlung eine Eigenschaft hinzu. |
| [clear()](#clear) | Entfernt alle Elemente aus der Sammlung. |
| [contains(String name)](#contains-java.lang.String) | Ermittelt, ob die Sammlung eine Eigenschaft mit dem angegebenen Namen enthält. |
| [get(int index)](#get-int) | Liest eine Eigenschaft am angegebenen Index. |
| [get(String name)](#get-java.lang.String) | Stellt Zugriff auf die Elemente der Sammlung bereit. |
| [getCount()](#getCount) | Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Gibt den nullbasierten Index der angegebenen Eigenschaft in der Sammlung zurück. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [remove(String name)](#remove-java.lang.String) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [removeAt(int index)](#removeAt-int) | Entfernt eine Eigenschaft am angegebenen Index. |
### add(CustomXmlProperty property) {#add-com.aspose.words.CustomXmlProperty}
```
public void add(CustomXmlProperty property)
```


Fügt der Sammlung eine Eigenschaft hinzu.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| property | [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) | Die hinzuzufügende Eigenschaft. |

### clear() {#clear}
```
public void clear()
```


Entfernt alle Elemente aus der Sammlung.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Ermittelt, ob die Sammlung eine Eigenschaft mit dem angegebenen Namen enthält.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Groß-/Kleinschreibung‑sensitiver Name der zu findenden Eigenschaft. |

**Returns:**
boolean -  true  wenn das Element in der Sammlung gefunden wird; andernfalls,  false .
### get(int index) {#get-int}
```
public CustomXmlProperty get(int index)
```


Liest eine Eigenschaft am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index der Eigenschaft. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty/) - A property at the specified index.
### get(String name) {#get-java.lang.String}
```
public CustomXmlProperty get(String name)
```


Bietet Zugriff auf die Elemente der Sammlung.  Liest eine Eigenschaft mit dem angegebenen Namen.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Groß-/Kleinschreibung‑sensitiver Name der zu findenden Eigenschaft. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty/) - The corresponding [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) value.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Returns:**
int – Die Anzahl der im Sammelobjekt enthaltenen Elemente.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Gibt den nullbasierten Index der angegebenen Eigenschaft in der Sammlung zurück.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der groß-/kleinschreibungssensible Name der Eigenschaft. |

**Returns:**
int - Der nullbasierte Index. Negativer Wert, wenn nicht gefunden.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
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

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der groß-/kleinschreibungssensible Name der Eigenschaft. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt eine Eigenschaft am angegebenen Index.

 **Examples:** 

Zeigt, wie man mit Smart-Tag-Eigenschaften arbeitet, um detaillierte Informationen über Smart Tags zu erhalten.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
 // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
 // In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
 // In our input document, there are three objects that Microsoft Word registered as smart tags.
 // Smart tags may be nested, so this collection contains more.
 List smartTags = Arrays.stream(doc.getChildNodes(NodeType.SMART_TAG, true).toArray())
         .filter(SmartTag.class::isInstance)
         .map(SmartTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(8, smartTags.size());

 // The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
 // The properties of a "date"-type smart tag contain its year, month, and day.
 CustomXmlPropertyCollection properties = smartTags.get(7).getProperties();

 Assert.assertEquals(4, properties.getCount());

 Iterator enumerator = properties.iterator();

 while (enumerator.hasNext()) {
     CustomXmlProperty customXmlProperty = enumerator.next();

     System.out.println(MessageFormat.format("Property name: {0}, value: {1}", customXmlProperty.getName(), customXmlProperty.getValue()));
     Assert.assertEquals("", enumerator.next().getUri());
 }

 // We can also access the properties in various ways, such as a key-value pair.
 Assert.assertTrue(properties.contains("Day"));
 Assert.assertEquals("22", properties.get("Day").getValue());
 Assert.assertEquals("2003", properties.get(2).getValue());
 Assert.assertEquals(1, properties.indexOfKey("Month"));

 // Below are three ways of removing elements from the properties collection.
 // 1 -  Remove by index:
 properties.removeAt(3);

 Assert.assertEquals(3, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Year");

 Assert.assertEquals(2, properties.getCount());

 // 3 -  Clear the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index. |

