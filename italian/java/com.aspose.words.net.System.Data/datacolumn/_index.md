---
title: "DataColumn"
linktitle: "DataColumn"
second_title: "Aspose.Words per Java"
description: "Rappresenta lo schema di una colonna in un DataTable in Java."
type: docs
weight: 14
url: /it/java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

Rappresenta lo schema di una colonna in un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [DataColumn()](#DataColumn) | Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) come tipo string. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), come tipo string, utilizzando il nome della colonna specificato. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Inizializza una nuova istanza della classe @\{link DataColumn\} utilizzando il nome della colonna specificato e la tabella a cui appartiene. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) utilizzando il nome della colonna specificato e il tipo di dati. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) utilizzando il nome della colonna specificato, il tipo di dati e la tabella a cui appartiene. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | Restituisce un valore che indica se i valori null sono consentiti in questa colonna per le righe che appartengono alla tabella. |
| [getAutoIncrement()](#getAutoIncrement) | Restituisce un valore che indica se la colonna incrementa automaticamente il valore della colonna per le nuove righe aggiunte alla tabella. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | Restituisce il valore iniziale per una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | Restituisce l'incremento utilizzato da una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true. |
| [getCaption()](#getCaption) | Restituisce la didascalia della colonna. |
| [getColumnMapping()](#getColumnMapping) | Restituisce il [MappingType](../../com.aspose.words.net.system.data/mappingtype/) della colonna. |
| [getColumnName()](#getColumnName) | Restituisce il nome della colonna nella [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getDataType()](#getDataType) | Restituisce il tipo di dati memorizzati nella colonna. |
| [getDefaultValue()](#getDefaultValue) | Restituisce il valore predefinito per la colonna quando si creano nuove righe. |
| [getExpression()](#getExpression) | Restituisce l'espressione usata per filtrare le righe, calcolare i valori in una colonna o creare una colonna aggregata. |
| [getMaxLength()](#getMaxLength) | Restituisce la lunghezza massima di una colonna di testo. |
| [getNamespace()](#getNamespace) | Restituisce lo spazio dei nomi del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [getOrdinal()](#getOrdinal) | Restituisce la posizione della colonna nella collezione [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getPrefix()](#getPrefix) | Restituisce un prefisso XML che alias lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getReadOnly()](#getReadOnly) | Restituisce un valore che indica se la colonna consente modifiche non appena una riga è stata aggiunta alla tabella. |
| [getTable()](#getTable) | Restituisce il [DataTable](../../com.aspose.words.net.system.data/datatable/) a cui appartiene la colonna. |
| [getUnique()](#getUnique) | Restituisce un valore che indica se i valori in ogni riga della colonna devono essere unici. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | Imposta un valore che indica se i valori null sono consentiti in questa colonna per le righe che appartengono alla tabella. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | Imposta un valore che indica se la colonna incrementa automaticamente il valore della colonna per le nuove righe aggiunte alla tabella. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | Imposta il valore iniziale per una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | Imposta l'incremento utilizzato da una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true. |
| [setCaption(String value)](#setCaption-java.lang.String) | Imposta la didascalia della colonna. |
| [setColumnMapping(int value)](#setColumnMapping-int) | Imposta il [MappingType](../../com.aspose.words.net.system.data/mappingtype/) della colonna. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | Imposta il nome della colonna nella [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [setDataType(Class value)](#setDataType-java.lang.Class) | Imposta il tipo di dati memorizzati nella colonna. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | Imposta il valore predefinito per la colonna quando si creano nuove righe. |
| [setMaxLength(int value)](#setMaxLength-int) | Imposta la lunghezza massima di una colonna di testo. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Imposta lo spazio dei nomi del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [setOrdinal(int ordinal)](#setOrdinal-int) | Modifica l'ordine o la posizione del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) all'ordine o alla posizione specificati. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | Imposta un prefisso XML che alias lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | Imposta un valore che indica se la colonna consente modifiche non appena una riga è stata aggiunta alla tabella. |
| [setUnique(boolean value)](#setUnique-boolean) | Imposta un valore che indica se i valori in ogni riga della colonna devono essere unici. |
| [toString()](#toString) | Ottiene il [getExpression()](../../com.aspose.words.net.system.data/datacolumn/#getExpression) della colonna, se esiste. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) come tipo string.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), come tipo string, utilizzando il nome della colonna specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | Una stringa che rappresenta il nome della colonna da creare. Se impostata a null o a una stringa vuota (""), verrà specificato un nome predefinito quando aggiunta alla raccolta di colonne. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


Inizializza una nuova istanza della classe @\{link DataColumn\} utilizzando il nome della colonna specificato e la tabella a cui appartiene.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | nome del DataColumn |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | la tabella a cui appartiene questa colonna |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) utilizzando il nome della colonna specificato e il tipo di dati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnName | java.lang.String | Una stringa che rappresenta il nome della colonna da creare. Se impostata a null o a una stringa vuota (""), verrà specificato un nome predefinito quando aggiunta alla raccolta di colonne. |
| dataType | java.lang.Class | Un [getDataType()](../../com.aspose.words.net.system.data/datacolumn/#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/#setDataType-java.lang.Class) supportato. |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


Inizializza una nuova istanza della classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) utilizzando il nome della colonna specificato, il tipo di dati e la tabella a cui appartiene.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | java.lang.String | nome del DataColumn |
| tipo | java.lang.Class | tipo di dati |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | la tabella a cui appartiene questa colonna |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


Restituisce un valore che indica se i valori null sono consentiti in questa colonna per le righe che appartengono alla tabella.

**Returns:**
boolean - true se i valori null sono consentiti; altrimenti, false. Il valore predefinito è true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


Restituisce un valore che indica se la colonna incrementa automaticamente il valore della colonna per le nuove righe aggiunte alla tabella.

**Returns:**
boolean - true se il valore della colonna si incrementa automaticamente; altrimenti, false. Il valore predefinito è false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


Restituisce il valore iniziale per una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true.

**Returns:**
long - Il valore iniziale per la funzionalità [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean).
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


Restituisce l'incremento utilizzato da una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true.

**Returns:**
long - Il numero di cui il valore della colonna viene incrementato automaticamente. Il valore predefinito è 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


Restituisce la didascalia della colonna.

**Returns:**
java.lang.String - La didascalia della colonna. Se non impostata, restituisce il valore di [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/#setColumnName-java.lang.String).
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


Restituisce il [MappingType](../../com.aspose.words.net.system.data/mappingtype/) della colonna.

**Returns:**
int - Uno dei valori di [MappingType](../../com.aspose.words.net.system.data/mappingtype/). Il valore restituito è una delle costanti di [MappingType](../../com.aspose.words.net.system.data/mappingtype/).
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


Restituisce il nome della colonna nella [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
java.lang.String - Il nome della colonna.
### getDataType() {#getDataType}
```
public Class getDataType()
```


Restituisce il tipo di dati memorizzati nella colonna.

**Returns:**
java.lang.Class - Un oggetto java.lang.Class che rappresenta il tipo di dati della colonna.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


Restituisce il valore predefinito per la colonna quando si creano nuove righe.

**Returns:**
java.lang.Object - Un valore appropriato al [getDataType()](../../com.aspose.words.net.system.data/datacolumn/#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/#setDataType-java.lang.Class) della colonna.
### getExpression() {#getExpression}
```
public String getExpression()
```


Restituisce l'espressione usata per filtrare le righe, calcolare i valori in una colonna o creare una colonna aggregata.

**Returns:**
java.lang.String - Un'espressione per calcolare il valore di una colonna, o creare una colonna aggregata. Il tipo di ritorno di un'espressione è determinato dal [getDataType()](../../com.aspose.words.net.system.data/datacolumn/#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/#setDataType-java.lang.Class) della colonna.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Restituisce la lunghezza massima di una colonna di testo.

**Returns:**
int - La lunghezza massima della colonna in caratteri. Se la colonna non ha una lunghezza massima, il valore è -1 (predefinito).
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Restituisce lo spazio dei nomi del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Returns:**
java.lang.String - Lo spazio dei nomi del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


Restituisce la posizione della colonna nella collezione [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
int - La posizione della colonna. Restituisce -1 se la colonna non è membro di una raccolta.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


Restituisce un prefisso XML che alias lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Il prefisso XML per lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


Restituisce un valore che indica se la colonna consente modifiche non appena una riga è stata aggiunta alla tabella.

**Returns:**
boolean - true se la colonna è di sola lettura; altrimenti, false. Il valore predefinito è false.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Restituisce il [DataTable](../../com.aspose.words.net.system.data/datatable/) a cui appartiene la colonna.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


Restituisce un valore che indica se i valori in ogni riga della colonna devono essere unici.

**Returns:**
boolean - true se il valore deve essere univoco; altrimenti, false. Il valore predefinito è false.
### isReadOnly() {#isReadOnly}
```
public boolean isReadOnly()
```




**Returns:**
boolean
### isUnique() {#isUnique}
```
public boolean isUnique()
```




**Returns:**
boolean
### setAllowDBNull(boolean value) {#setAllowDBNull-boolean}
```
public void setAllowDBNull(boolean value)
```


Imposta un valore che indica se i valori null sono consentiti in questa colonna per le righe che appartengono alla tabella.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | true se i valori null sono consentiti; altrimenti, false. Il valore predefinito è true. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


Imposta un valore che indica se la colonna incrementa automaticamente il valore della colonna per le nuove righe aggiunte alla tabella.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | true se il valore della colonna viene incrementato automaticamente; altrimenti, false. Il valore predefinito è false. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


Imposta il valore iniziale per una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | long | Il valore iniziale per la funzionalità [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean). |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


Imposta l'incremento utilizzato da una colonna la cui proprietà [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/#setAutoIncrement-boolean) è impostata su true.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | long | Il numero con cui il valore della colonna viene incrementato automaticamente. Il valore predefinito è 1. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Imposta la didascalia della colonna.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | La didascalia della colonna. Se non impostata, restituisce il valore di [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String). |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


Imposta il [MappingType](../../com.aspose.words.net.system.data/mappingtype/) della colonna.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Uno dei valori di [MappingType](../../com.aspose.words.net.system.data/mappingtype/) . Il valore deve essere una delle costanti di [MappingType](../../com.aspose.words.net.system.data/mappingtype/). |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


Imposta il nome della colonna nella [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome della colonna. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


Imposta il tipo di dati memorizzati nella colonna.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.Class | Un oggetto java.lang.Class che rappresenta il tipo di dati della colonna. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


Imposta il valore predefinito per la colonna quando si creano nuove righe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.Object | Un valore appropriato al [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Imposta la lunghezza massima di una colonna di testo.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La lunghezza massima della colonna in caratteri. Se la colonna non ha una lunghezza massima, il valore è -1 (predefinito). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Imposta lo spazio dei nomi del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | Lo spazio dei nomi del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


Modifica l'ordine o la posizione del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) all'ordine o alla posizione specificati.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'ordinal specificato. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


Imposta un prefisso XML che alias lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | Il prefisso XML per lo spazio dei nomi del [DataTable](../../com.aspose.words.net.system.data/datatable/) namespace. |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


Imposta un valore che indica se la colonna consente modifiche non appena una riga è stata aggiunta alla tabella.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | true se la colonna è di sola lettura; altrimenti, false. Il valore predefinito è false. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


Imposta un valore che indica se i valori in ogni riga della colonna devono essere unici.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | true se il valore deve essere univoco; altrimenti, false. Il valore predefinito è false. |

### toString() {#toString}
```
public String toString()
```


Ottiene il [getExpression()](../../com.aspose.words.net.system.data/datacolumn/#getExpression) della colonna, se esiste.

**Returns:**
java.lang.String - Il valore di [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) se la proprietà è impostata; altrimenti, la proprietà [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
