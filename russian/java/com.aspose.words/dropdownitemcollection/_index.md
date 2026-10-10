---
title: "DropDownItemCollection"
linktitle: "DropDownItemCollection"
second_title: "Aspose.Words для Java"
description: "Коллекция строк, представляющих все элементы выпадающего поля формы в Java."
type: docs
weight: 178
url: /ru/java/com.aspose.words/dropdownitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DropDownItemCollection implements Iterable
```

Коллекция строк, представляющих все элементы выпадающего поля формы.

Чтобы узнать больше, посетите статью документации [ Working with Fields ][Working with Fields].

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
## Методы

| Метод | Описание |
| --- | --- |
| [add(String value)](#add-java.lang.String) |  |
| [clear()](#clear) | Удаляет все элементы из коллекции. |
| [contains(String value)](#contains-java.lang.String) | Определяет, содержит ли коллекция указанное значение. |
| [get(int index)](#get-int) | Получает элемент по указанному индексу. |
| [getCount()](#getCount) | Получает количество элементов, содержащихся в коллекции. |
| [indexOf(String value)](#indexOf-java.lang.String) | Возвращает индекс, начинающийся с нуля, указанного значения в коллекции. |
| [insert(int index, String value)](#insert-int-java.lang.String) | Вставляет строку в коллекцию по указанному индексу. |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [iterator()](#iterator) | Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции. |
| [remove(String name)](#remove-java.lang.String) | Удаляет указанное значение из коллекции. |
| [removeAt(int index)](#removeAt-int) | Удаляет значение по указанному индексу. |
| [set(int index, String value)](#set-int-java.lang.String) | Устанавливает элемент по указанному индексу. |
### add(String value) {#add-java.lang.String}
```
public int add(String value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String |  |

**Returns:**
int
### clear() {#clear}
```
public void clear()
```


Удаляет все элементы из коллекции.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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


Определяет, содержит ли коллекция указанное значение.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Регистрозависимое значение для поиска. |

**Returns:**
boolean -  true  если элемент найден в коллекции; иначе,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Получает элемент по указанному индексу.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
java.lang.String - Элемент по указанному индексу.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество элементов, содержащихся в коллекции.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
int — количество элементов, содержащихся в коллекции.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Возвращает индекс, начинающийся с нуля, указанного значения в коллекции.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Регистрозависимое значение для поиска. |

**Returns:**
int - Индекс, начинающийся с нуля. Отрицательное значение, если не найден.
### insert(int index, String value) {#insert-int-java.lang.String}
```
public void insert(int index, String value)
```


Вставляет строку в коллекцию по указанному индексу.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс, по которому значение вставляется. |
| значение | java.lang.String | Строка для вставки. |

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


Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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


Удаляет указанное значение из коллекции.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Регистрозависимое значение для удаления. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет значение по указанному индексу.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Устанавливает элемент по указанному индексу.

 **Examples:** 

Показывает, как вставить поле комбобокса и отредактировать элементы в его коллекции элементов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |
| значение | java.lang.String | Элемент по указанному индексу. |

