---
title: "VariableCollection"
linktitle: "VariableCollection"
second_title: "Aspose.Words pour Java"
description: "Une collection de variables de document en Java."
type: docs
weight: 703
url: /fr/java/com.aspose.words/variablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VariableCollection implements Iterable
```

Une collection de variables de document.

Pour en savoir plus, consultez l’article de documentation [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

Les noms de variables et les valeurs sont des chaînes.

Les noms de variables ne sont pas sensibles à la casse.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(String name, String value)](#add-java.lang.String-java.lang.String) | Ajoute une variable de document à la collection. |
| [clear()](#clear) | Supprime tous les éléments de la collection. |
| [contains(String name)](#contains-java.lang.String) | Détermine si la collection contient une variable de document avec le nom donné. |
| [get(int index)](#get-int) | Obtient une variable de document à l'indice spécifié. |
| [get(String name)](#get-java.lang.String) | Fournit l'accès aux éléments de la collection. |
| [getCount()](#getCount) | Obtient le nombre d'éléments contenus dans la collection. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Renvoie l'index basé sur zéro de la variable de document spécifiée dans la collection. |
| [iterator()](#iterator) | Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les variables de la collection. |
| [remove(String name)](#remove-java.lang.String) | Supprime une variable de document portant le nom spécifié de la collection. |
| [removeAt(int index)](#removeAt-int) | Supprime une variable de document à l'index spécifié. |
| [set(int index, String value)](#set-int-java.lang.String) | Définit une variable de document à l'index spécifié. |
| [set(String name, String value)](#set-java.lang.String-java.lang.String) | Fournit l'accès aux éléments de la collection. |
### add(String name, String value) {#add-java.lang.String-java.lang.String}
```
public void add(String name, String value)
```


Ajoute une variable de document à la collection.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la variable à ajouter, insensible à la casse. |
| valeur | java.lang.String | La valeur de la variable. La valeur ne peut pas être  null , si la valeur est null une chaîne vide sera utilisée à la place. |

### clear() {#clear}
```
public void clear()
```


Supprime tous les éléments de la collection.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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


Détermine si la collection contient une variable de document avec le nom donné.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Nom de la variable de document à localiser, insensible à la casse. |

**Returns:**
booléen -  true  si l'élément est trouvé dans la collection ; sinon,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Obtient une variable de document à l'index spécifié.  null  les valeurs ne sont pas autorisées du côté droit de l'affectation et seront remplacées par une chaîne vide.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Index basé sur zéro de la variable de document. |

**Returns:**
java.lang.String - Une variable de document à l'index spécifié.
### get(String name) {#get-java.lang.String}
```
public String get(String name)
```


Fournit l'accès aux éléments de la collection.  Obtient ou définit une variable de document par le nom insensible à la casse.  null  les valeurs ne sont pas autorisées du côté droit de l'affectation et seront remplacées par une chaîne vide.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String |  |

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments contenus dans la collection.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
int - Le nombre d'éléments contenus dans la collection.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Renvoie l'index basé sur zéro de la variable de document spécifiée dans la collection.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la variable, insensible à la casse. |

**Returns:**
int - L'index basé sur zéro. Valeur négative si non trouvé.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les variables de la collection.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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


Supprime une variable de document portant le nom spécifié de la collection.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom de la variable, insensible à la casse. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime une variable de document à l'index spécifié.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Définit une variable de document à l'index spécifié.  null  les valeurs ne sont pas autorisées du côté droit de l'affectation et seront remplacées par une chaîne vide.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Index basé sur zéro de la variable de document. |
| valeur | java.lang.String | Une variable de document à l'index spécifié. |

### set(String name, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String name, String value)
```


Fournit l'accès aux éléments de la collection.  Obtient ou définit une variable de document par le nom insensible à la casse.  null  les valeurs ne sont pas autorisées du côté droit de l'affectation et seront remplacées par une chaîne vide.

 **Examples:** 

Montre comment travailler avec la collection de variables d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String |  |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

