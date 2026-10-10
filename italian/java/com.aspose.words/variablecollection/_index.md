---
title: "VariableCollection"
linktitle: "VariableCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di variabili del documento in Java."
type: docs
weight: 703
url: /it/java/com.aspose.words/variablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VariableCollection implements Iterable
```

Una raccolta di variabili del documento.

Per saperne di più, visita l'articolo di documentazione [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

I nomi delle variabili e i valori sono stringhe.

I nomi delle variabili non distinguono tra maiuscole e minuscole.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(String name, String value)](#add-java.lang.String-java.lang.String) | Aggiunge una variabile del documento alla raccolta. |
| [clear()](#clear) | Rimuove tutti gli elementi dalla raccolta. |
| [contains(String name)](#contains-java.lang.String) | Determina se la raccolta contiene una variabile del documento con il nome fornito. |
| [get(int index)](#get-int) | Ottiene una variabile del documento all'indice specificato. |
| [get(String name)](#get-java.lang.String) | Fornisce l'accesso agli elementi della raccolta. |
| [getCount()](#getCount) | Ottiene il numero di elementi contenuti nella collezione. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Restituisce l'indice basato su zero della variabile di documento specificata nella raccolta. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore che può essere usato per iterare su tutte le variabili nella raccolta. |
| [remove(String name)](#remove-java.lang.String) | Rimuove una variabile di documento con il nome specificato dalla raccolta. |
| [removeAt(int index)](#removeAt-int) | Rimuove una variabile di documento all'indice specificato. |
| [set(int index, String value)](#set-int-java.lang.String) | Imposta una variabile di documento all'indice specificato. |
| [set(String name, String value)](#set-java.lang.String-java.lang.String) | Fornisce l'accesso agli elementi della raccolta. |
### add(String name, String value) {#add-java.lang.String-java.lang.String}
```
public void add(String name, String value)
```


Aggiunge una variabile del documento alla raccolta.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome non sensibile a maiuscole/minuscole della variabile da aggiungere. |
| valore | java.lang.String | Il valore della variabile. Il valore non può essere  null , se il valore è null verrà usata una stringa vuota. |

### clear() {#clear}
```
public void clear()
```


Rimuove tutti gli elementi dalla raccolta.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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


Determina se la raccolta contiene una variabile del documento con il nome fornito.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Nome non sensibile a maiuscole/minuscole della variabile di documento da individuare. |

**Returns:**
boolean -  true  se l'elemento è trovato nella collezione; altrimenti,  false .
### get(int index) {#get-int}
```
public String get(int index)
```


Ottiene una variabile di documento all'indice specificato.  null  i valori non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero della variabile di documento. |

**Returns:**
java.lang.String - Una variabile di documento all'indice specificato.
### get(String name) {#get-java.lang.String}
```
public String get(String name)
```


Fornisce l'accesso agli elementi della raccolta.  Ottiene o imposta una variabile di documento per nome non sensibile a maiuscole/minuscole.  null  i valori non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di elementi contenuti nella collezione.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
int - Il numero di elementi contenuti nella collezione.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Restituisce l'indice basato su zero della variabile di documento specificata nella raccolta.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome non sensibile a maiuscole/minuscole della variabile. |

**Returns:**
int - L'indice basato su zero. Valore negativo se non trovato.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore che può essere usato per iterare su tutte le variabili nella raccolta.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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


Rimuove una variabile di documento con il nome specificato dalla raccolta.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome non sensibile a maiuscole/minuscole della variabile. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove una variabile di documento all'indice specificato.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero. |

### set(int index, String value) {#set-int-java.lang.String}
```
public void set(int index, String value)
```


Imposta una variabile di documento all'indice specificato.  null  i valori non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Indice basato su zero della variabile di documento. |
| valore | java.lang.String | Una variabile di documento all'indice specificato. |

### set(String name, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String name, String value)
```


Fornisce l'accesso agli elementi della raccolta.  Ottiene o imposta una variabile di documento per nome non sensibile a maiuscole/minuscole.  null  i valori non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota.

 **Examples:** 

Mostra come lavorare con la raccolta di variabili di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String |  |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

