---
title: "DataColumnCollection"
linktitle: "DataColumnCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una collezione di oggetti DataColumn per un DataTable in Java."
type: docs
weight: 15
url: /it/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

Rappresenta una collezione di oggetti [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) per un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | Crea e aggiunge l'oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) specificato alla [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName)](#add-java.lang.String) | Crea e aggiunge un oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con il nome specificato alla [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | Crea e aggiunge un oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con il nome e il tipo specificati alla [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | Crea e aggiunge un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con il nome, il tipo e i valori specifici alla collezione di colonne. |
| [clear()](#clear) | Cancella dalla collezione tutte le colonne. |
| [contains(String name)](#contains-java.lang.String) | Verifica se la collezione contiene una colonna con il nome specificato. |
| [get(int index)](#get-int) | Restituisce il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) dalla collezione all'indice specificato. |
| [get(String name)](#get-java.lang.String) | Restituisce il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) dalla collezione con il nome specificato. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | Restituisce l'indice di una colonna specificata per nome. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | Restituisce l'indice della colonna con il nome specifico (il nome non distingue tra maiuscole e minuscole). |
| [iterator()](#iterator) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | Rimuove l'oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) specificato dalla collezione. |
| [remove(String name)](#remove-java.lang.String) | Rimuove l'oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che ha il nome specificato dalla collezione. |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


Crea e aggiunge l'oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) specificato alla [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da aggiungere. |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


Crea e aggiunge un oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con il nome specificato alla [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | Il nome della colonna. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


Crea e aggiunge un oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con il nome e il tipo specificati alla [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | Il [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) da utilizzare quando crei la colonna. |
| type | java.lang.Class | Il [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) della nuova colonna. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


Crea e aggiunge un [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) con il nome, il tipo e i valori specifici alla collezione di colonne.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | name |
| tipo | java.lang.Class | tipo di dati |
| columnMapping | int | tipo di mapping della colonna |
| allowAutoIncrement | boolean | l'incremento automatico è consentito |
| allowDBNull | boolean | è consentito il valore DBNull |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


Cancella dalla collezione tutte le colonne.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Verifica se la collezione contiene una colonna con il nome specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) della colonna da cercare. |

**Returns:**
boolean - true se esiste una colonna con questo nome; altrimenti, false.
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


Restituisce il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) dalla collezione all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero della colonna da restituire. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


Restituisce il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) dalla collezione con il nome specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) della colonna da restituire. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - il numero totale di elementi in una collezione.
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


Restituisce l'indice di una colonna specificata per nome.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il nome della colonna da restituire. |

**Returns:**
int - L'indice della colonna specificata da  column  se trovata; altrimenti, -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


Restituisce l'indice della colonna con il nome specifico (il nome non distingue tra maiuscole e minuscole).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | Il nome della colonna da trovare. |

**Returns:**
int - L'indice basato su zero della colonna con il nome specificato, o -1 se la colonna non esiste nella collezione.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


Rimuove l'oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) specificato dalla collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Il [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) da rimuovere. |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Rimuove l'oggetto [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) che ha il nome specificato dalla collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome della colonna da rimuovere. |

