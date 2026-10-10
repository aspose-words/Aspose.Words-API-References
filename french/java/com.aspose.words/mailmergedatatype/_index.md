---
title: "MailMergeDataType"
linktitle: "MailMergeDataType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'une source de données de fusion de courrier externe en Java."
type: docs
weight: 440
url: /fr/java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

Spécifie le type d'une source de données de publipostage externe.
## Champs

| Champ | Description |
| --- | --- |
| [DATABASE](#DATABASE) | Spécifie qu'un document donné a été connecté à une base de données Access via le système Dynamic Data Exchange (DDE). |
| [DEFAULT](#DEFAULT) | Égal à [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | Spécifie qu'un document donné a été connecté à une source de données externe via l'interface Office Data Source Object (ODSO). |
| [NONE](#NONE) | Aucune source de données de fusion de courrier n'est spécifiée. |
| [ODBC](#ODBC) | Spécifie qu'un document donné a été connecté à une source de données externe via l'interface Open Database Connectivity. |
| [QUERY](#QUERY) | Spécifie qu'un document donné a été connecté à une source de données externe à l'aide d'un outil de requête externe. |
| [SPREADSHEET](#SPREADSHEET) | Spécifie qu'un document donné a été connecté à une feuille de calcul Excel via le système Dynamic Data Exchange (DDE). |
| [TEXT_FILE](#TEXT-FILE) | Spécifie qu'un document donné a été connecté à un fichier texte via le système Dynamic Data Exchange (DDE). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Spécifie qu'un document donné a été connecté à une base de données Access via le système Dynamic Data Exchange (DDE).

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Égal à [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Spécifie qu'un document donné a été connecté à une source de données externe via l'interface Office Data Source Object (ODSO).

### NONE {#NONE}
```
public static int NONE
```


Aucune source de données de fusion de courrier n'est spécifiée.

### ODBC {#ODBC}
```
public static int ODBC
```


Spécifie qu'un document donné a été connecté à une source de données externe via l'interface Open Database Connectivity.

### QUERY {#QUERY}
```
public static int QUERY
```


Spécifie qu'un document donné a été connecté à une source de données externe à l'aide d'un outil de requête externe.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Spécifie qu'un document donné a été connecté à une feuille de calcul Excel via le système Dynamic Data Exchange (DDE).

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Spécifie qu'un document donné a été connecté à un fichier texte via le système Dynamic Data Exchange (DDE).

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
