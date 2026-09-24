---
title: "MailMergeDataType"
linktitle: "MailMergeDataType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de una fuente de datos de combinación de correspondencia externa en Java."
type: docs
weight: 440
url: /es/java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

Especifica el tipo de un origen de datos externo de combinación de correspondencia.
## Campos

| Campo | Descripción |
| --- | --- |
| [DATABASE](#DATABASE) | Especifica que un documento dado ha sido conectado a una base de datos Access mediante el sistema Dynamic Data Exchange (DDE). |
| [DEFAULT](#DEFAULT) | Equivale a [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | Especifica que un documento dado ha sido conectado a una fuente de datos externa mediante la interfaz Office Data Source Object (ODSO). |
| [NONE](#NONE) | No se ha especificado ninguna fuente de datos de combinación de correspondencia. |
| [ODBC](#ODBC) | Especifica que un documento dado ha sido conectado a una fuente de datos externa mediante la interfaz Open Database Connectivity. |
| [QUERY](#QUERY) | Especifica que un documento dado ha sido conectado a una fuente de datos externa usando una herramienta de consulta externa. |
| [SPREADSHEET](#SPREADSHEET) | Especifica que un documento dado ha sido conectado a una hoja de cálculo Excel mediante el sistema Dynamic Data Exchange (DDE). |
| [TEXT_FILE](#TEXT-FILE) | Especifica que un documento dado ha sido conectado a un archivo de texto mediante el sistema Dynamic Data Exchange (DDE). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Especifica que un documento dado ha sido conectado a una base de datos Access mediante el sistema Dynamic Data Exchange (DDE).

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equivale a [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Especifica que un documento dado ha sido conectado a una fuente de datos externa mediante la interfaz Office Data Source Object (ODSO).

### NONE {#NONE}
```
public static int NONE
```


No se ha especificado ninguna fuente de datos de combinación de correspondencia.

### ODBC {#ODBC}
```
public static int ODBC
```


Especifica que un documento dado ha sido conectado a una fuente de datos externa mediante la interfaz Open Database Connectivity.

### QUERY {#QUERY}
```
public static int QUERY
```


Especifica que un documento dado ha sido conectado a una fuente de datos externa usando una herramienta de consulta externa.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Especifica que un documento dado ha sido conectado a una hoja de cálculo Excel mediante el sistema Dynamic Data Exchange (DDE).

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Especifica que un documento dado ha sido conectado a un archivo de texto mediante el sistema Dynamic Data Exchange (DDE).

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
