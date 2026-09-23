---
title: "XmlReadMode"
linktitle: "XmlReadMode"
second_title: "Aspose.Words per Java"
description: "Specifica come leggere i dati XML e uno schema relazionale in un DataSet in Java."
type: docs
weight: 37
url: /it/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

Specifica come leggere i dati XML e uno schema relazionale in un [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | Predefinito. |
| [DIFF_GRAM](#DIFF-GRAM) | Legge un DiffGram, applicando le modifiche dal DiffGram al [DataSet](../../com.aspose.words.net.system.data/dataset/) e preservando i valori di [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState). |
| [FRAGMENT](#FRAGMENT) | Legge frammenti XML, come quelli generati dall'esecuzione di query FOR XML, contro un'istanza di SQL Server. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | Ignora qualsiasi schema inline e legge i dati nello schema esistente del [DataSet](../../com.aspose.words.net.system.data/dataset/) schema. |
| [INFER_SCHEMA](#INFER-SCHEMA) | Ignora qualsiasi schema inline, deduce lo schema dai dati e carica i dati. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | Ignora qualsiasi schema inline, deduce uno schema tipizzato fortemente dai dati e carica i dati. |
| [READ_SCHEMA](#READ-SCHEMA) | Legge qualsiasi schema inline e carica i dati. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String) |  |
| [compareTo(E arg0)](#compareTo-E) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getDeclaringClass()](#getDeclaringClass) |  |
| [hashCode()](#hashCode) |  |
| [name()](#name) |  |
| [ordinal()](#ordinal) |  |
| [toString()](#toString) |  |
| [valueOf(String name)](#valueOf-java.lang.String) |  |
| [values()](#values) |  |
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


Predefinito.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


Legge un DiffGram, applicando le modifiche dal DiffGram al [DataSet](../../com.aspose.words.net.system.data/dataset/) e preservando i valori di [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState).

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


Legge frammenti XML, come quelli generati dall'esecuzione di query FOR XML, su un'istanza di SQL Server. Quando [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) è impostato su Fragment, lo spazio dei nomi predefinito viene letto come schema inline.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


Ignora qualsiasi schema inline e legge i dati nello schema esistente del [DataSet](../../com.aspose.words.net.system.data/dataset/). Se qualche dato non corrisponde allo schema esistente, viene scartato (inclusi i dati provenienti da spazi dei nomi differenti definiti per il [DataSet](../../com.aspose.words.net.system.data/dataset/)). Se i dati sono un DiffGram, IgnoreSchema ha la stessa funzionalità di DiffGram.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


Ignora qualsiasi schema inline, deduce lo schema dai dati e carica i dati. Se il [DataSet](../../com.aspose.words.net.system.data/dataset/) contiene già uno schema, lo schema corrente viene esteso aggiungendo nuove tabelle o aggiungendo colonne alle tabelle esistenti. Viene generata un'eccezione se la tabella dedotta esiste già ma con uno spazio dei nomi diverso, o se una delle colonne dedotte entra in conflitto con colonne esistenti.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


Ignora qualsiasi schema inline, deduce uno schema tipizzato fortemente dai dati e carica i dati. Se il tipo non può essere dedotto dai dati, viene interpretato come dati stringa. Se il [DataSet](../../com.aspose.words.net.system.data/dataset/) contiene già uno schema, lo schema corrente viene esteso, sia aggiungendo nuove tabelle sia aggiungendo colonne alle tabelle esistenti. Viene generata un'eccezione se la tabella dedotta esiste già ma con uno spazio dei nomi diverso, o se una delle colonne dedotte entra in conflitto con colonne esistenti.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


Legge qualsiasi schema inline e carica i dati. Se il [DataSet](../../com.aspose.words.net.system.data/dataset/) contiene già uno schema, nuove tabelle possono essere aggiunte allo schema, ma viene generata un'eccezione se qualche tabella nello schema inline esiste già nel [DataSet](../../com.aspose.words.net.system.data/dataset/).

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Returns:**
T
### compareTo(E arg0) {#compareTo-E}
```
public final int compareTo(E arg0)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getDeclaringClass() {#getDeclaringClass}
```
public final Class<E> getDeclaringClass()
```




**Returns:**
java.lang.Class<E>
### hashCode() {#hashCode}
```
public final int hashCode()
```




**Returns:**
int
### name() {#name}
```
public final String name()
```




**Returns:**
java.lang.String
### ordinal() {#ordinal}
```
public final int ordinal()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String}
```
public static System.Data.XmlReadMode valueOf(String name)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/)
### values() {#values}
```
public static System.Data.XmlReadMode[] values()
```




**Returns:**
com.aspose.words.net.System.Data.XmlReadMode[]
