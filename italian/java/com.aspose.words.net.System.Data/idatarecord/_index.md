---
title: "IDataRecord"
linktitle: "IDataRecord"
second_title: "Aspose.Words per Java"
description: "Fornisce l'accesso ai valori delle colonne all'interno di ogni riga per un DataReader ed è implementato dai provider di dati del .NET Framework che accedono a database relazionali in Java."
type: docs
weight: 35
url: /it/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

Fornisce l'accesso ai valori delle colonne all'interno di ogni riga per un DataReader, ed è implementato dai provider di dati .NET Framework che accedono a database relazionali.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int i)](#get-int) | Ottiene la colonna situata all'indice specificato. |
| [getFieldCount()](#getFieldCount) | Ottiene il numero di colonne nella riga corrente. |
| [getFieldType(int i)](#getFieldType-int) | Ottiene le informazioni java.lang.Class corrispondenti al tipo di java.lang.Object che verrebbe restituito da [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int). |
| [getName(int i)](#getName-int) | Ottiene il nome del campo da trovare. |
| [getValue(int i)](#getValue-int) | Restituisce il valore del campo specificato. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


Ottiene la colonna situata all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| i | int | L'indice basato su zero della colonna da ottenere. |

**Returns:**
java.lang.Object - La colonna situata all'indice specificato come un java.lang.Object.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


Ottiene il numero di colonne nella riga corrente.

**Returns:**
int - Quando non è posizionato in un recordset valido, 0; altrimenti, il numero di colonne nel record corrente. Il valore predefinito è -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


Ottiene le informazioni java.lang.Class corrispondenti al tipo di java.lang.Object che verrebbe restituito da [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| i | int | L'indice del campo da trovare. |

**Returns:**
java.lang.Class - Le informazioni java.lang.Class corrispondenti al tipo di java.lang.Object che verrebbe restituito da [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


Ottiene il nome del campo da trovare.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| i | int | L'indice del campo da trovare. |

**Returns:**
java.lang.String - Il nome del campo o la stringa vuota (\"\"), se non c'è alcun valore da restituire.
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


Restituisce il valore del campo specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| i | int | L'indice del campo da trovare. |

**Returns:**
java.lang.Object - Il java.lang.Object che conterrà il valore del campo al ritorno.
