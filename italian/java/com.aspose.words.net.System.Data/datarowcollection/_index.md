---
title: "DataRowCollection"
linktitle: "DataRowCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di righe per un DataTable in Java."
type: docs
weight: 21
url: /it/java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

Rappresenta una raccolta di righe per il [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | Aggiunge il [DataRow](../../com.aspose.words.net.system.data/datarow/) specificato all'oggetto [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [add(Object[] values)](#add-java.lang.Object...) | Crea una riga utilizzando i valori specificati e la aggiunge al [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [clear()](#clear) | Cancella tutte le righe dalla raccolta. |
| [find(Object[] keys)](#find-java.lang.Object) | Restituisce la riga che contiene i valori della chiave primaria specificati. |
| [find(String primaryKeyValue)](#find-java.lang.String) | Restituisce la riga specificata dal valore della chiave primaria. |
| [get(int index)](#get-int) | Restituisce la riga all'indice specificato. |
| [get(Object[] values)](#get-java.lang.Object) | Restituisce la riga che contiene i valori specificati. |
| [getCount()](#getCount) | Restituisce il numero totale di oggetti [DataRow](../../com.aspose.words.net.system.data/datarow/) in questa raccolta. |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | Inserisce una nuova riga nella raccolta nella posizione specificata. |
| [iterator()](#iterator) | Restituisce un java.util.Iterator per questa raccolta. |
| [removeAt(int index)](#removeAt-int) | Rimuove la riga all'indice specificato dalla raccolta. |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


Aggiunge il [DataRow](../../com.aspose.words.net.system.data/datarow/) specificato all'oggetto [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Il [DataRow](../../com.aspose.words.net.system.data/datarow/) da aggiungere. |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


Crea una riga utilizzando i valori specificati e la aggiunge al [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valori | java.lang.Object[] | L'array di valori utilizzato per creare la nuova riga. |

### clear() {#clear}
```
public void clear()
```


Cancella tutte le righe dalla raccolta.

### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


Restituisce la riga che contiene i valori della chiave primaria specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chiavi | java.lang.Object[] | Un array di valori di chiave primaria da trovare. Il tipo dell'array è Object. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Restituisce la riga specificata dal valore della chiave primaria.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | Il valore della chiave primaria del DataRow da trovare. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


Restituisce la riga all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero della riga da restituire. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


Ottiene la riga che contiene i valori specificati. Se sono presenti le colonne della chiave primaria, verrà utilizzato l'indice. Se non c'è indice, verrà eseguita una scansione lineare semplice. Fai attenzione a questo perché potrebbe richiedere molto tempo.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valori | java.lang.Object[] | dati della riga |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero totale di oggetti [DataRow](../../com.aspose.words.net.system.data/datarow/) in questa raccolta.

**Returns:**
int - Il numero totale di oggetti [DataRow](../../com.aspose.words.net.system.data/datarow/) in questa collezione.
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Inserisce una nuova riga nella raccolta nella posizione specificata.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Il [DataRow](../../com.aspose.words.net.system.data/datarow/) da aggiungere. |
| pos | int | La posizione (basata su zero) nella collezione dove vuoi aggiungere il DataRow. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un java.util.Iterator per questa raccolta.

**Returns:**
java.util.Iterator - Un java.util.Iterator per questa collezione.
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove la riga all'indice specificato dalla raccolta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice della riga da rimuovere. |

