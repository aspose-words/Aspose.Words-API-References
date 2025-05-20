---
title: VariableCollection
linktitle: VariableCollection
second_title: Aspose.Words for Java
description: A collection of document variables in Java.
type: docs
weight: 691
url: /java/com.aspose.words/variablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VariableCollection implements Iterable
```

A collection of document variables.

To learn more, visit the [ Work with Document Properties ][Work with Document Properties] documentation article.

 **Remarks:** 

Variable names and values are strings.

Variable names are case-insensitive.

 **Examples:** 

Shows how to work with a document's variable collection.

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
## Methods

| Method | Description |
| --- | --- |
| [add(String name, String value)](#add-java.lang.String-java.lang.String) | Adds a document variable to the collection. |
| [clear()](#clear) | Removes all elements from the collection. |
| [contains(String name)](#contains-java.lang.String) | Determines whether the collection contains a document variable with the given name. |
| [get(int index)](#get-int) | Gets a document variable at the specified index. |
| [get(String name)](#get-java.lang.String) | Provides access to the collection items. |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Returns the zero-based index of the specified document variable in the collection. |
| [iterator()](#iterator) | Returns an enumerator object that can be used to iterate over all variable in the collection. |
| [remove(String name)](#remove-java.lang.String) | Removes a document variable with the specified name from the collection. |
| [removeAt(int index)](#removeAt-int) | Removes a document variable at the specified index. |
| [set(int index, String value)](#set-int-java.lang.String) | Sets a document variable at the specified index. |
| [set(String name, String value)](#set-java.lang.String-java.lang.String) | Provides access to the collection items. |
### add(String name, String value) {#add-java.lang.String-java.lang.String}
```
public void add(String name, String value)
```


Adds a document variable to the collection.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the variable to add. |
| value | java.lang.String | The value of the variable. The value cannot be  null , if value is null empty string will be used instead. |

### clear() {#clear}
```
public void clear()
```


Removes all elements from the collection.

 **Examples:** 

Shows how to work with a document's variable collection.

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


Determines whether the collection contains a document variable with the given name.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the document variable to locate. |

**Returns:**
boolean -  true  if item is found in the collection; otherwise,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Gets a document variable at the specified index.  null  values are not allowed as a right hand side of the assignment and will be replaced by empty string.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the document variable. |

**Returns:**
java.lang.String - A document variable at the specified index.
### get(String name) {#get-java.lang.String}
```
public String get(String name)
```


Provides access to the collection items.  Gets or a sets a document variable by the case-insensitive name.  null  values are not allowed as a right hand side of the assignment and will be replaced by empty string.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

 **Examples:** 

Shows how to work with a document's variable collection.

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
int - The number of elements contained in the collection.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Returns the zero-based index of the specified document variable in the collection.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the variable. |

**Returns:**
int - The zero based index. Negative value if not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object that can be used to iterate over all variable in the collection.

 **Examples:** 

Shows how to work with a document's variable collection.

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


Removes a document variable with the specified name from the collection.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the variable. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a document variable at the specified index.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Sets a document variable at the specified index.  null  values are not allowed as a right hand side of the assignment and will be replaced by empty string.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the document variable. |
| value | java.lang.String | A document variable at the specified index. |

### set(String name, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String name, String value)
```


Provides access to the collection items.  Gets or a sets a document variable by the case-insensitive name.  null  values are not allowed as a right hand side of the assignment and will be replaced by empty string.

 **Examples:** 

Shows how to work with a document's variable collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |
| value | java.lang.String | The corresponding java.lang.String value. |

