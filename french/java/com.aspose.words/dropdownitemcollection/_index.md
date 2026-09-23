---
title: "DropDownItemCollection"
linktitle: "DropDownItemCollection"
second_title: "Aspose.Words pour Java"
description: "Une collection de chaînes qui représente tous les éléments d'un champ de formulaire déroulant en Java."
type: docs
weight: 178
url: /fr/java/com.aspose.words/dropdownitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DropDownItemCollection implements Iterable
```

Une collection de chaînes représentant tous les éléments d'un champ de formulaire déroulant.

Pour en savoir plus, consultez l'article de documentation [ Working with Fields ][Working with Fields].

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(String value)](#add-java.lang.String) |  |
| [clear()](#clear) | Supprime tous les éléments de la collection. |
| [contains(String value)](#contains-java.lang.String) | Détermine si la collection contient la valeur spécifiée. |
| [get(int index)](#get-int) | Obtient l'élément à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre d'éléments contenus dans la collection. |
| [indexOf(String value)](#indexOf-java.lang.String) | Renvoie l'index basé sur zéro de la valeur spécifiée dans la collection. |
| [insert(int index, String value)](#insert-int-java.lang.String) | Insère une chaîne dans la collection à l'index spécifié. |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [iterator()](#iterator) | Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [remove(String name)](#remove-java.lang.String) | Supprime la valeur spécifiée de la collection. |
| [removeAt(int index)](#removeAt-int) | Supprime une valeur à l'index spécifié. |
| [set(int index, String value)](#set-int-java.lang.String) | Définit l'élément à l'index spécifié. |
### add(String value) {#add-java.lang.String}
```
public int add(String value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String |  |

**Returns:**
int
### clear() {#clear}
```
public void clear()
```


Supprime tous les éléments de la collection.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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


Détermine si la collection contient la valeur spécifiée.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Valeur sensible à la casse à localiser. |

**Returns:**
boolean -  true  si l'élément est trouvé dans la collection ; sinon,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Obtient l'élément à l'index spécifié.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
java.lang.String - L'élément à l'index spécifié.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments contenus dans la collection.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
int - Le nombre d'éléments contenus dans la collection.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Renvoie l'index basé sur zéro de la valeur spécifiée dans la collection.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur sensible à la casse à localiser. |

**Returns:**
int - L'index basé sur zéro. Valeur négative si non trouvé.
### insert(int index, String value) {#insert-int-java.lang.String}
```
public void insert(int index, String value)
```


Insère une chaîne dans la collection à l'index spécifié.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro où la valeur est insérée. |
| valeur | java.lang.String | La chaîne à insérer. |

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


Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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


Supprime la valeur spécifiée de la collection.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | La valeur sensible à la casse à supprimer. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime une valeur à l'index spécifié.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Définit l'élément à l'index spécifié.

 **Examples:** 

Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |
| valeur | java.lang.String | L'élément à l'index spécifié. |

