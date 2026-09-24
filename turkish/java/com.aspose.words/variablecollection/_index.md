---
title: "VariableCollection"
linktitle: "VariableCollection"
second_title: "Aspose.Words Java için"
description: "Java'da belge değişkenlerinin bir koleksiyonu."
type: docs
weight: 703
url: /tr/java/com.aspose.words/variablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VariableCollection implements Iterable
```

Belge değişkenlerinin bir koleksiyonu.

Daha fazla bilgi edinmek için, [ Work with Document Properties ][Work with Document Properties] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Değişken adları ve değerleri stringtir.

Değişken adları büyük/küçük harfe duyarsızdır.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(String name, String value)](#add-java.lang.String-java.lang.String) | Bir belge değişkenini koleksiyona ekler. |
| [clear()](#clear) | Koleksiyondaki tüm öğeleri kaldırır. |
| [contains(String name)](#contains-java.lang.String) | Koleksiyonun verilen ada sahip bir belge değişkeni içerip içermediğini belirler. |
| [get(int index)](#get-int) | Belirtilen indeksteki belge değişkenini alır. |
| [get(String name)](#get-java.lang.String) | Koleksiyon öğelerine erişim sağlar. |
| [getCount()](#getCount) | Koleksiyonda bulunan öğe sayısını alır. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Belirtilen belge değişkeninin koleksiyondaki sıfır tabanlı indeksini döndürür. |
| [iterator()](#iterator) | Koleksiyondaki tüm değişkenler üzerinde yineleme yapmak için kullanılabilecek bir enumerator nesnesi döndürür. |
| [remove(String name)](#remove-java.lang.String) | Belirtilen ada sahip bir belge değişkenini koleksiyondan kaldırır. |
| [removeAt(int index)](#removeAt-int) | Belirtilen indeksteki bir belge değişkenini kaldırır. |
| [set(int index, String value)](#set-int-java.lang.String) | Belirtilen indeksteki bir belge değişkenini ayarlar. |
| [set(String name, String value)](#set-java.lang.String-java.lang.String) | Koleksiyon öğelerine erişim sağlar. |
### add(String name, String value) {#add-java.lang.String-java.lang.String}
```
public void add(String name, String value)
```


Bir belge değişkenini koleksiyona ekler.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Eklenecek değişkenin büyük/küçük harfe duyarsız adı. |
| değer | java.lang.String | Değişkenin değeri. Değer `null` olamaz, değer `null` ise boş string kullanılacaktır. |

### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm öğeleri kaldırır.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Koleksiyonun verilen ada sahip bir belge değişkeni içerip içermediğini belirler.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak belge değişkeninin büyük/küçük harfe duyarsız adı. |

**Returns:**
boolean - öğe koleksiyonda bulunursa true; aksi takdirde false.
### get(int index) {#get-int}
```
public String get(int index)
```


Belirtilen indeksteki bir belge değişkenini alır. `null` değerler atamanın sağ tarafında izin verilmez ve boş string ile değiştirilir.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Belge değişkeninin sıfır tabanlı indeksi. |

**Returns:**
java.lang.String - Belirtilen indeksteki bir belge değişkeni.
### get(String name) {#get-java.lang.String}
```
public String get(String name)
```


Koleksiyon öğelerine erişim sağlar. Büyük/küçük harfe duyarsız adla bir belge değişkeni alır veya ayarlar. `null` değerler atamanın sağ tarafında izin verilmez ve boş string ile değiştirilir.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyonda bulunan öğe sayısını alır.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Returns:**
int - Koleksiyonda bulunan öğe sayısı.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Belirtilen belge değişkeninin koleksiyondaki sıfır tabanlı indeksini döndürür.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Değişkenin büyük/küçük harfe duyarsız adı. |

**Returns:**
int - Sıfır tabanlı indeks. Bulunamazsa negatif değer.
### iterator() {#iterator}
```
public Iterator iterator()
```


Koleksiyondaki tüm değişkenler üzerinde yineleme yapmak için kullanılabilecek bir enumerator nesnesi döndürür.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Belirtilen ada sahip bir belge değişkenini koleksiyondan kaldırır.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Değişkenin büyük/küçük harfe duyarsız adı. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Belirtilen indeksteki bir belge değişkenini kaldırır.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Sıfır tabanlı indeks. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Belirtilen indeksteki bir belge değişkenini ayarlar. `null` değerler atamanın sağ tarafında izin verilmez ve boş string ile değiştirilir.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Belge değişkeninin sıfır tabanlı indeksi. |
| değer | java.lang.String | Belirtilen indeksteki bir belge değişkeni. |

### set(String name, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String name, String value)
```


Koleksiyon öğelerine erişim sağlar. Büyük/küçük harfe duyarsız adla bir belge değişkeni alır veya ayarlar. `null` değerler atamanın sağ tarafında izin verilmez ve boş string ile değiştirilir.

 **Examples:** 

Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String |  |
| değer | java.lang.String | İlgili java.lang.String değeri. |

