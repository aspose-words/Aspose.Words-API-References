---
title: "DataTableCollection"
linktitle: "DataTableCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta la collezione di tabelle per il DataSet in Java."
type: docs
weight: 26
url: /it/java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

Rappresenta la collezione di tabelle per il [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | Aggiunge il DataTable specificato alla collezione. |
| [add(String name)](#add-java.lang.String) | Crea un oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) utilizzando il nome specificato e lo aggiunge alla collezione. |
| [contains(String name)](#contains-java.lang.String) | Restituisce un valore che indica se un oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato esiste nella collezione. |
| [get(int index)](#get-int) | Restituisce l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) all'indice specificato. |
| [get(String name)](#get-java.lang.String) | Restituisce l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Restituisce l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato nello spazio dei nomi specificato. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | Rimuove l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato dalla collezione. |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


Aggiunge il DataTable specificato alla collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | L'oggetto DataTable da aggiungere. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


Crea un oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) utilizzando il nome specificato e lo aggiunge alla collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome da assegnare al [DataTable](../../com.aspose.words.net.system.data/datatable/) creato. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Restituisce un valore che indica se un oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato esiste nella collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del [DataTable](../../com.aspose.words.net.system.data/datatable/) da trovare. |

**Returns:**
boolean - true se la tabella specificata esiste; altrimenti false.
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


Restituisce l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int | L'indice basato su zero del [DataTable](../../com.aspose.words.net.system.data/datatable/) da trovare. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


Restituisce l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del DataTable da trovare. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


Restituisce l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato nello spazio dei nomi specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome del DataTable da trovare. |
| tableNamespace | java.lang.String | Il nome dello spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/) in cui cercare. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - numero totale di elementi in questa collezione.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public System.Data.DataTable remove(String name)
```


Rimuove l'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) con il nome specificato dalla collezione.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | Il nome dell'oggetto [DataTable](../../com.aspose.words.net.system.data/datatable/) da rimuovere. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
