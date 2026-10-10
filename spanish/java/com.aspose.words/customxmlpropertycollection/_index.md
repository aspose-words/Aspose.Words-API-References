---
title: "CustomXmlPropertyCollection"
linktitle: "CustomXmlPropertyCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de atributos XML personalizados o propiedades de etiquetas inteligentes en Java."
type: docs
weight: 146
url: /es/java/com.aspose.words/customxmlpropertycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlPropertyCollection implements Iterable
```

Representa una colección de atributos XML personalizados o propiedades de etiqueta inteligente.

Para obtener más información, visite el artículo de documentación [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Los elementos son objetos [CustomXmlProperty](../../com.aspose.words/customxmlproperty/).

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(CustomXmlProperty property)](#add-com.aspose.words.CustomXmlProperty) | Agrega una propiedad a la colección. |
| [clear()](#clear) | Elimina todos los elementos de la colección. |
| [contains(String name)](#contains-java.lang.String) | Determina si la colección contiene una propiedad con el nombre dado. |
| [get(int index)](#get-int) | Obtiene una propiedad en el índice especificado. |
| [get(String name)](#get-java.lang.String) | Proporciona acceso a los elementos de la colección. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Devuelve el índice basado en cero de la propiedad especificada en la colección. |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [remove(String name)](#remove-java.lang.String) | Elimina una propiedad con el nombre especificado de la colección. |
| [removeAt(int index)](#removeAt-int) | Elimina una propiedad en el índice especificado. |
### add(CustomXmlProperty property) {#add-com.aspose.words.CustomXmlProperty}
```
public void add(CustomXmlProperty property)
```


Agrega una propiedad a la colección.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| property | [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) | La propiedad a agregar. |

### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos de la colección.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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


Determina si la colección contiene una propiedad con el nombre dado.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | Nombre sensible a mayúsculas y minúsculas de la propiedad a localizar. |

**Returns:**
boolean -  true  si el elemento se encuentra en la colección; de lo contrario,  false .
### get(int index) {#get-int}
```
public CustomXmlProperty get(int index)
```


Obtiene una propiedad en el índice especificado.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Índice basado en cero de la propiedad. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty/) - A property at the specified index.
### get(String name) {#get-java.lang.String}
```
public CustomXmlProperty get(String name)
```


Proporciona acceso a los elementos de la colección.  Obtiene una propiedad con el nombre especificado.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | Nombre sensible a mayúsculas y minúsculas de la propiedad a localizar. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty/) - The corresponding [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) value.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
int - El número de elementos contenidos en la colección.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Devuelve el índice basado en cero de la propiedad especificada en la colección.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre sensible a mayúsculas y minúsculas de la propiedad. |

**Returns:**
int - El índice basado en cero. Valor negativo si no se encuentra.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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


Elimina una propiedad con el nombre especificado de la colección.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre sensible a mayúsculas y minúsculas de la propiedad. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina una propiedad en el índice especificado.

 **Examples:** 

Muestra cómo trabajar con propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero. |

