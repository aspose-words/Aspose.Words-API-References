---
title: "MailMergeDataType"
linktitle: "MailMergeDataType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di una sorgente dati di stampa unione esterna in Java."
type: docs
weight: 440
url: /it/java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

Specifica il tipo di una fonte dati di stampa unione esterna.
## Campi

| Campo | Descrizione |
| --- | --- |
| [DATABASE](#DATABASE) | Specifica che un determinato documento è stato collegato a un database Access tramite il sistema Dynamic Data Exchange (DDE). |
| [DEFAULT](#DEFAULT) | Uguale a [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | Specifica che un determinato documento è stato collegato a una sorgente dati esterna tramite l'interfaccia Office Data Source Object (ODSO). |
| [NONE](#NONE) | Nessuna sorgente dati di stampa unione è specificata. |
| [ODBC](#ODBC) | Specifica che un determinato documento è stato collegato a una sorgente dati esterna tramite l'interfaccia Open Database Connectivity. |
| [QUERY](#QUERY) | Specifica che un determinato documento è stato collegato a una sorgente dati esterna utilizzando uno strumento di query esterno. |
| [SPREADSHEET](#SPREADSHEET) | Specifica che un determinato documento è stato collegato a un foglio di calcolo Excel tramite il sistema Dynamic Data Exchange (DDE). |
| [TEXT_FILE](#TEXT-FILE) | Specifica che un determinato documento è stato collegato a un file di testo tramite il sistema Dynamic Data Exchange (DDE). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Specifica che un determinato documento è stato collegato a un database Access tramite il sistema Dynamic Data Exchange (DDE).

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Uguale a [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Specifica che un determinato documento è stato collegato a una sorgente dati esterna tramite l'interfaccia Office Data Source Object (ODSO).

### NONE {#NONE}
```
public static int NONE
```


Nessuna sorgente dati di stampa unione è specificata.

### ODBC {#ODBC}
```
public static int ODBC
```


Specifica che un determinato documento è stato collegato a una sorgente dati esterna tramite l'interfaccia Open Database Connectivity.

### QUERY {#QUERY}
```
public static int QUERY
```


Specifica che un determinato documento è stato collegato a una sorgente dati esterna utilizzando uno strumento di query esterno.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Specifica che un determinato documento è stato collegato a un foglio di calcolo Excel tramite il sistema Dynamic Data Exchange (DDE).

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Specifica che un determinato documento è stato collegato a un file di testo tramite il sistema Dynamic Data Exchange (DDE).

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDataType) {#toString-int}
```
public static String toString(int mailMergeDataType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
