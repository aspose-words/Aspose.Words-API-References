---
title: "OdsoDataSourceType"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di origine dati esterna a cui connettersi come parte delle informazioni di connessione ODSO in Java."
type: docs
weight: 488
url: /it/java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

Specifica il tipo della fonte dati esterna a cui connettersi come parte delle informazioni di connessione ODSO.

 **Remarks:** 

La specifica OOXML è molto vaga per questa enumerazione. Immagino che possa corrispondere all'enumerazione WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Campi

| Campo | Descrizione |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Specifica che un determinato documento è stato collegato a una rubrica di contatti. |
| [DATABASE](#DATABASE) | Specifica che un determinato documento è stato collegato a un database. |
| [DEFAULT](#DEFAULT) | Uguale a [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | Specifica che un determinato documento è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. |
| [DOCUMENT_2](#DOCUMENT-2) | Specifica che un determinato documento è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. |
| [EMAIL](#EMAIL) | Specifica che un determinato documento è stato collegato a un'applicazione di posta elettronica. |
| [LEGACY](#LEGACY) | Specifica che un determinato documento è stato collegato a un formato di documento legacy supportato dall'applicazione produttrice. Probabilmente wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Specifica che un determinato documento è stato collegato a una fonte dati che aggrega altre fonti dati. |
| [NATIVE](#NATIVE) | Specifica che un determinato documento è stato collegato a un altro formato di documento nativo dell'applicazione produttrice. |
| [NONE](#NONE) | Il tipo della fonte dati esterna non è specificato. |
| [TEXT](#TEXT) | Specifica che un determinato documento è stato collegato a un file di testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Specifica che un determinato documento è stato collegato a una rubrica di contatti. Probabilmente wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Specifica che un determinato documento è stato collegato a un database. Probabilmente wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Uguale a [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Specifica che un determinato documento è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. Probabilmente wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Specifica che un determinato documento è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. Probabilmente wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Specifica che un determinato documento è stato collegato a un'applicazione di posta elettronica. Probabilmente wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Specifica che un determinato documento è stato collegato a un formato di documento legacy supportato dall'applicazione produttrice. Probabilmente wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Specifica che un determinato documento è stato collegato a una fonte dati che aggrega altre fonti dati.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Specifica che un determinato documento è stato collegato a un altro formato di documento nativo dell'applicazione produttrice. Probabilmente wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


Il tipo della fonte dati esterna non è specificato. Probabilmente wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


Specifica che un determinato documento è stato collegato a un file di testo. Probabilmente wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odsoDataSourceType) {#toString-int}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
