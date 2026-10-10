---
title: "DropDownItemCollection"
linktitle: "DropDownItemCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di stringhe che rappresentano tutti gli elementi in un campo modulo a discesa in Java."
type: docs
weight: 178
url: /it/java/com.aspose.words/dropdownitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DropDownItemCollection implements Iterable
```

Una collezione di stringhe che rappresentano tutti gli elementi in un campo modulo a discesa.

Per saperne di più, visita l'articolo di documentazione [ Working with Fields ][Working with Fields].

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(String value)](#add-java.lang.String) |  |
| [clear()](#clear) | Rimuove tutti gli elementi dalla raccolta. |
| [contains(String value)](#contains-java.lang.String) | Determina se la raccolta contiene il valore specificato. |
| [get(int index)](#get-int) | Ottiene l'elemento all'indice specificato. |
| [getCount()](#getCount) | Ottiene il numero di elementi contenuti nella collezione. |
| [indexOf(String value)](#indexOf-java.lang.String) | Restituisce l'indice basato su zero del valore specificato nella raccolta. |
| [insert(int index, String value)](#insert-int-java.lang.String) | Inserisce una stringa nella raccolta all'indice specificato. |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [iterator()](#iterator) | Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione. |
| [remove(String name)](#remove-java.lang.String) | Rimuove il valore specificato dalla raccolta. |
| [removeAt(int index)](#removeAt-int) | Rimuove un valore all'indice specificato. |
| [set(int index, String value)](#set-int-java.lang.String) | Imposta l'elemento all'indice specificato. |
### add(String value) {#add-java.lang.String}
```
public int add(String value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String |  |

**Returns:**
int
### clear() {#clear}
```
public void clear()
```


Rimuove tutti gli elementi dalla raccolta.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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


Determina se la raccolta contiene il valore specificato.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Valore sensibile al maiuscolo/minuscolo da individuare. |

**Returns:**
boolean -  true  se l'elemento è trovato nella raccolta; altrimenti,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Ottiene l'elemento all'indice specificato.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
java.lang.String - L'elemento all'indice specificato.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di elementi contenuti nella collezione.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
int - Il numero di elementi contenuti nella collezione.
### indexOf(String value) {#indexOf-java.lang.String}
```
public int indexOf(String value)
```


Restituisce l'indice basato su zero del valore specificato nella raccolta.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore sensibile al maiuscolo/minuscolo da individuare. |

**Returns:**
int - L'indice basato su zero. Valore negativo se non trovato.
### insert(int index, String value) {#insert-int-java.lang.String}
```
public void insert(int index, String value)
```


Inserisce una stringa nella raccolta all'indice specificato.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero al quale il valore è inserito. |
| valore | java.lang.String | La stringa da inserire. |

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


Restituisce un oggetto iteratore che può essere usato per iterare su tutti gli elementi nella collezione.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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


Rimuove il valore specificato dalla raccolta.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il valore sensibile al maiuscolo/minuscolo da rimuovere. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove un valore all'indice specificato.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Imposta l'elemento all'indice specificato.

 **Examples:** 

Mostra come inserire un campo combo box e modificare gli elementi nella sua collezione di elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |
| valore | java.lang.String | L'elemento all'indice specificato. |

