---
title: "DocumentPropertyCollection"
linktitle: "DocumentPropertyCollection"
second_title: "Aspose.Words Java için"
description: "Java'da BuiltInDocumentProperties ve CustomDocumentProperties koleksiyonları için temel sınıftır."
type: docs
weight: 169
url: /tr/java/com.aspose.words/documentpropertycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public abstract class DocumentPropertyCollection implements Iterable
```

[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/) ve [CustomDocumentProperties](../../com.aspose.words/customdocumentproperties/) koleksiyonları için temel sınıftır.

Daha fazla bilgi edinmek için, [ Work with Document Properties ][Work with Document Properties] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Özellik adları büyük/küçük harfe duyarsızdır.

Koleksiyondaki özellikler ada göre alfabetik olarak sıralanır.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DocumentPropertyCollection()](#DocumentPropertyCollection) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clear()](#clear) | Koleksiyondaki tüm özellikleri kaldırır. |
| [contains(String name)](#contains-java.lang.String) | Koleksiyonda belirtilen ada sahip bir özellik varsa  true  döndürür. |
| [get(int index)](#get-int) | Dizine göre bir [DocumentProperty](../../com.aspose.words/documentproperty/) nesnesi döndürür. |
| [get(String name)](#get-java.lang.String) | Koleksiyon öğelerine erişim sağlar. |
| [getCount()](#getCount) | Koleksiyondaki öğe sayısını alır. |
| [indexOf(String name)](#indexOf-java.lang.String) | Bir özelliğin adına göre dizinini alır. |
| [iterator()](#iterator) | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür. |
| [remove(String name)](#remove-java.lang.String) | Belirtilen ada sahip bir özelliği koleksiyondan kaldırır. |
| [removeAt(int index)](#removeAt-int) | Belirtilen dizindeki bir özelliği kaldırır. |
### DocumentPropertyCollection() {#DocumentPropertyCollection}
```
public DocumentPropertyCollection()
```


### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm özellikleri kaldırır.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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


Koleksiyonda belirtilen ada sahip bir özellik varsa  true  döndürür.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Özelliğin büyük/küçük harfe duyarsız adı. |

**Returns:**
boolean -  true  eğer özellik koleksiyonda mevcutsa;  false  aksi takdirde.
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Dizine göre bir [DocumentProperty](../../com.aspose.words/documentproperty/) nesnesi döndürür.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Özel belge özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int | Alınacak [DocumentProperty](../../com.aspose.words/documentproperty/) nesnesinin sıfır tabanlı dizini. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Koleksiyon öğelerine erişim sağlar.  Özelliğin adına göre bir [DocumentProperty](../../com.aspose.words/documentproperty/) nesnesi döndürür.

 **Remarks:** 

Belirtilen ada sahip bir özellik bulunamazsa  null  döndürür.

 **Examples:** 

Tarih ve saat içeren bir özel belge özelliğinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Alınacak özelliğin büyük/küçük harfe duyarsız adı. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki öğe sayısını alır.

 **Examples:** 

Özel belge özellikleriyle nasıl çalışılacağını gösterir.

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
int - Koleksiyondaki öğe sayısı.
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Bir özelliğin adına göre dizinini alır.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Özelliğin büyük/küçük harfe duyarsız adı. |

**Returns:**
int - Sıfır tabanlı indeks. Bulunamazsa negatif değer.
### iterator() {#iterator}
```
public Iterator iterator()
```


Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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


Belirtilen ada sahip bir özelliği koleksiyondan kaldırır.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Özelliğin büyük/küçük harfe duyarsız adı. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Belirtilen dizindeki bir özelliği kaldırır.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Sıfır tabanlı indeks. |

