---
title: "CustomXmlPropertyCollection"
linktitle: "CustomXmlPropertyCollection"
second_title: "Aspose.Words Java için"
description: "Java'da özel XML öznitelikleri veya akıllı etiket özelliklerinden oluşan bir koleksiyonu temsil eder."
type: docs
weight: 146
url: /tr/java/com.aspose.words/customxmlpropertycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlPropertyCollection implements Iterable
```

Özel XML özniteliklerinin veya akıllı etiket özelliklerinin bir koleksiyonunu temsil eder.

Daha fazla bilgi için, [ Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü ][Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Ögeler [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) nesneleridir.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(CustomXmlProperty property)](#add-com.aspose.words.CustomXmlProperty) | Koleksiyona bir özellik ekler. |
| [clear()](#clear) | Koleksiyondaki tüm öğeleri kaldırır. |
| [contains(String name)](#contains-java.lang.String) | Koleksiyonun verilen ada sahip bir özellik içerip içermediğini belirler. |
| [get(int index)](#get-int) | Belirtilen indeksteki bir özelliği alır. |
| [get(String name)](#get-java.lang.String) | Koleksiyon öğelerine erişim sağlar. |
| [getCount()](#getCount) | Koleksiyonda bulunan öğe sayısını alır. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Koleksiyondaki belirtilen özelliğin sıfır tabanlı indeksini döndürür. |
| [iterator()](#iterator) | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür. |
| [remove(String name)](#remove-java.lang.String) | Belirtilen ada sahip bir özelliği koleksiyondan kaldırır. |
| [removeAt(int index)](#removeAt-int) | Belirtilen dizindeki bir özelliği kaldırır. |
### add(CustomXmlProperty property) {#add-com.aspose.words.CustomXmlProperty}
```
public void add(CustomXmlProperty property)
```


Koleksiyona bir özellik ekler.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| property | [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) | Eklenecek özellik. |

### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm öğeleri kaldırır.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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


Koleksiyonun verilen ada sahip bir özellik içerip içermediğini belirler.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak özelliğin büyük/küçük harfe duyarlı adı. |

**Returns:**
boolean -  true  eğer öğe koleksiyonda bulunursa; aksi takdirde,  false .
### get(int index) {#get-int}
```
public CustomXmlProperty get(int index)
```


Belirtilen indeksteki bir özelliği alır.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Özelliğin sıfır tabanlı indeksi. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty/) - A property at the specified index.
### get(String name) {#get-java.lang.String}
```
public CustomXmlProperty get(String name)
```


Koleksiyon öğelerine erişim sağlar.  Belirtilen ada sahip bir özelliği alır.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak özelliğin büyük/küçük harfe duyarlı adı. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty/) - The corresponding [CustomXmlProperty](../../com.aspose.words/customxmlproperty/) value.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyonda bulunan öğe sayısını alır.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
int - Koleksiyonda bulunan öğe sayısı.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Koleksiyondaki belirtilen özelliğin sıfır tabanlı indeksini döndürür.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Özelliğin büyük/küçük harfe duyarlı adı. |

**Returns:**
int - Sıfır tabanlı indeks. Bulunamazsa negatif değer.
### iterator() {#iterator}
```
public Iterator iterator()
```


Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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


Belirtilen ada sahip bir özelliği koleksiyondan kaldırır.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Özelliğin büyük/küçük harfe duyarlı adı. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Belirtilen dizindeki bir özelliği kaldırır.

 **Examples:** 

Akıllı etiketler hakkında derinlemesine bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Sıfır tabanlı indeks. |

