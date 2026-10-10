---
title: "DataRelationCollection"
linktitle: "DataRelationCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta la raccolta di oggetti DataRelation per questo DataSet in Java."
type: docs
weight: 19
url: /it/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

Rappresenta la raccolta di oggetti [DataRelation](../../com.aspose.words.net.system.data/datarelation/) per questo [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con una colonna padre e figlia specificate, e lo aggiunge alla raccolta. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | Aggiunge un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) alla [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | Aggiunge una relazione alla raccolta. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Aggiunge una relazione alla raccolta. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con il nome specificato, e le colonne padre e figlia, e lo aggiunge alla raccolta. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con il nome specificato, le colonne padre e figlia, con vincoli opzionali in base al valore del parametro  createConstraints , e lo aggiunge alla raccolta. |
| [clear()](#clear) | Cancella dalla raccolta tutte le relazioni. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | Verifica se un DataRelation con il nome specifico (non sensibile a maiuscole/minuscole) esiste nella raccolta. |
| [get(int index)](#get-int) | Ottiene l'oggetto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) all'indice specificato. |
| [get(String name)](#get-java.lang.String) | Ottiene l'oggetto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) specificato per nome. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | Ottiene l'indice dell'oggetto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) specificato. |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | Rimuove la relazione all'indice specificato dalla raccolta. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con una colonna padre e figlia specificate, e lo aggiunge alla raccolta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonna padre della relazione. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonna figlia della relazione. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


Aggiunge un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) alla [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Il DataRelation da aggiungere alla raccolta. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Aggiunge una relazione alla raccolta. Non esegue controlli su duplicati ecc.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabella padre della relazione. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabella figlia della relazione. |
| parentColumnName | java.lang.String | Il nome della colonna padre della relazione. |
| childColumnName | java.lang.String | Il nome della colonna figlio della relazione. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Aggiunge una relazione alla raccolta. Non esegue controlli su duplicati ecc.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabella padre della relazione. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabella figlia della relazione. |
| parentColumnNames | java.lang.String[] | L'array dei nomi delle colonne padre della relazione. |
| childColumnNames | java.lang.String[] | L'array dei nomi delle colonne figlio della relazione. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con il nome specificato, e le colonne padre e figlia, e lo aggiunge alla raccolta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della relazione. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonna padre della relazione. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonna figlia della relazione. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Crea un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) con il nome specificato, le colonne padre e figlia, con vincoli opzionali in base al valore del parametro  createConstraints , e lo aggiunge alla raccolta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della relazione. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonna padre della relazione. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | La colonna figlia della relazione. |
| createConstraints | boolean | true per creare vincoli; altrimenti false. (Il valore predefinito è true). |

### clear() {#clear}
```
public void clear()
```


Cancella dalla raccolta tutte le relazioni.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


Verifica se un DataRelation con il nome specifico (non sensibile a maiuscole/minuscole) esiste nella raccolta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Il nome della relazione da trovare. |

**Returns:**
boolean - true, se esiste una relazione con il nome specificato; altrimenti false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


Ottiene l'oggetto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero da trovare. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


Ottiene l'oggetto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) specificato per nome.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della relazione da trovare. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - il numero totale di elementi in una collezione
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


Ottiene l'indice dell'oggetto [DataRelation](../../com.aspose.words.net.system.data/datarelation/) specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | La relazione da cercare. |

**Returns:**
int - L'indice basato su zero della relazione, o -1 se la relazione non è trovata nella collezione.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove la relazione all'indice specificato dalla raccolta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice della relazione da rimuovere. |

