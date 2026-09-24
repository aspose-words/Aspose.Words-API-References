---
title: "DropDownItemCollection"
linktitle: "DropDownItemCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de cadenas que representan todos los elementos en un campo de formulario desplegable en Java."
type: docs
weight: 178
url: /es/java/com.aspose.words/dropdownitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DropDownItemCollection implements Iterable
```

Una colección de cadenas que representan todos los elementos en un campo de formulario desplegable.

Para obtener más información, visite el artículo de documentación [ Working with Fields ][Working with Fields].

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(String value)](#add-java.lang.String) |  |
| [clear()](#clear) | Elimina todos los elementos de la colección. |
| [contains(String value)](#contains-java.lang.String) | Determina si la colección contiene el valor especificado. |
| [get(int index)](#get-int) | Obtiene el elemento en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
| [indexOf(String value)](#indexOf-java.lang.String) | Devuelve el índice basado en cero del valor especificado en la colección. |
| [insert(int index, String value)](#insert-int-java.lang.String) | Inserta una cadena en la colección en el índice especificado. |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [remove(String name)](#remove-java.lang.String) | Elimina el valor especificado de la colección. |
| [removeAt(int index)](#removeAt-int) | Elimina un valor en el índice especificado. |
| [set(int index, String value)](#set-int-java.lang.String) | Establece el elemento en el índice especificado. |
### add(String value) {#add-java.lang.String}
```
public int add(String value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String |  |

**Returns:**
int
### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos de la colección.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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


Determina si la colección contiene el valor especificado.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Valor sensible a mayúsculas y minúsculas para localizar. |

**Returns:**
boolean -  true  si el elemento se encuentra en la colección; de lo contrario,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Obtiene el elemento en el índice especificado.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
java.lang.String - El elemento en el índice especificado.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
int - El número de elementos contenidos en la colección.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Devuelve el índice basado en cero del valor especificado en la colección.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor sensible a mayúsculas y minúsculas para localizar. |

**Returns:**
int - El índice basado en cero. Valor negativo si no se encuentra.
### insert(int index, String value) {#insert-int-java.lang.String}
```
public void insert(int index, String value)
```


Inserta una cadena en la colección en el índice especificado.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero en el que se inserta el valor. |
| valor | java.lang.String | La cadena a insertar. |

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


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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


Elimina el valor especificado de la colección.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El valor sensible a mayúsculas y minúsculas para eliminar. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina un valor en el índice especificado.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Establece el elemento en el índice especificado.

 **Examples:** 

Muestra cómo insertar un campo de combo box y editar los elementos en su colección de ítems.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |
| valor | java.lang.String | El elemento en el índice especificado. |

