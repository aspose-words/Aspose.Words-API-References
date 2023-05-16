---
title: DropDownItemCollection
linktitle: DropDownItemCollection
second_title: Aspose.Words for Java
description: A collection of strings that represent all the items in a drop-down form field in Java.
type: docs
weight: 146
url: /java/com.aspose.words/dropdownitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DropDownItemCollection implements Iterable
```

A collection of strings that represent all the items in a drop-down form field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [add(String value)](#add-java.lang.String) |  |
| [clear()](#clear) | Removes all elements from the collection. |
| [contains(String value)](#contains-java.lang.String) | Determines whether the collection contains the specified value. |
| [get(int index)](#get-int) | Gets the element at the specified index. |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [indexOf(String value)](#indexOf-java.lang.String) | Returns the zero-based index of the specified value in the collection. |
| [insert(int index, String value)](#insert-int-java.lang.String) | Inserts a string into the collection at the specified index. |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [iterator()](#iterator) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [remove(String name)](#remove-java.lang.String) | Removes the specified value from the collection. |
| [removeAt(int index)](#removeAt-int) | Removes a value at the specified index. |
| [set(int index, String value)](#set-int-java.lang.String) | Sets the element at the specified index. |
### add(String value) {#add-java.lang.String}
```
public int add(String value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String |  |

**Returns:**
int
### clear() {#clear}
```
public void clear()
```


Removes all elements from the collection.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

### contains(String value) {#contains-java.lang.String}
```
public boolean contains(String value)
```


Determines whether the collection contains the specified value.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Case-sensitive value to locate. |

**Returns:**
boolean -  true  if the item is found in the collection; otherwise,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Gets the element at the specified index.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
java.lang.String - The element at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Returns:**
int - The number of elements contained in the collection.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Returns the zero-based index of the specified value in the collection.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The case-sensitive value to locate. |

**Returns:**
int - The zero based index. Negative value if not found.
### insert(int index, String value) {#insert-int-java.lang.String}
```
public void insert(int index, String value)
```


Inserts a string into the collection at the specified index.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index at which value is inserted. |
| value | java.lang.String | The string to insert. |

### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Removes the specified value from the collection.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-sensitive value to remove. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a value at the specified index.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Sets the element at the specified index.

 **Examples:** 

Shows how to insert a combo box field, and edit the elements in its item collection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a combo box, and then verify its collection of drop-down items.
 // In Microsoft Word, the user will click the combo box,
 // and then choose one of the items of text in the collection to display.
 String[] items = {"One", "Two", "Three"};
 FormField comboBoxField = builder.insertComboBox("DropDown", items, 0);
 DropDownItemCollection dropDownItems = comboBoxField.getDropDownItems();

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertEquals("One", dropDownItems.get(0));
 Assert.assertEquals(1, dropDownItems.indexOf("Two"));
 Assert.assertTrue(dropDownItems.contains("Three"));

 // There are two ways of adding a new item to an existing collection of drop-down box items.
 // 1 -  Append an item to the end of the collection:
 dropDownItems.add("Four");

 // 2 -  Insert an item before another item at a specified index:
 dropDownItems.insert(3, "Three and a half");

 Assert.assertEquals(5, dropDownItems.getCount());

 // Iterate over the collection and print every element.
 Iterator dropDownCollectionEnumerator = dropDownItems.iterator();

 while (dropDownCollectionEnumerator.hasNext())
     System.out.println(dropDownCollectionEnumerator.next());

 // There are two ways of removing elements from a collection of drop-down items.
 // 1 -  Remove an item with contents equal to the passed string:
 dropDownItems.remove("Four");

 // 2 -  Remove an item at an index:
 dropDownItems.removeAt(3);

 Assert.assertEquals(3, dropDownItems.getCount());
 Assert.assertFalse(dropDownItems.contains("Three and a half"));
 Assert.assertFalse(dropDownItems.contains("Four"));

 doc.save(getArtifactsDir() + "FormFields.DropDownItemCollection.html");

 // Empty the whole collection of drop-down items.
 dropDownItems.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | java.lang.String | The element at the specified index. |

