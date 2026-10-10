---
title: "MailMergeDataType"
linktitle: "MailMergeDataType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ einer externen Seriendruck-Datenquelle in Java an."
type: docs
weight: 440
url: /de/java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

Gibt den Typ einer externen Seriendruck‑Datenquelle an.
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DATABASE](#DATABASE) | Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Access-Datenbank verbunden wurde. |
| [DEFAULT](#DEFAULT) | Entspricht [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | Gibt an, dass ein bestimmtes Dokument über die Office Data Source Object (ODSO)-Schnittstelle mit einer externen Datenquelle verbunden wurde. |
| [NONE](#NONE) | Keine Seriendruck-Datenquelle ist angegeben. |
| [ODBC](#ODBC) | Gibt an, dass ein bestimmtes Dokument über die Open Database Connectivity-Schnittstelle mit einer externen Datenquelle verbunden wurde. |
| [QUERY](#QUERY) | Gibt an, dass ein bestimmtes Dokument mit einer externen Datenquelle über ein externes Abfragewerkzeug verbunden wurde. |
| [SPREADSHEET](#SPREADSHEET) | Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Excel-Tabelle verbunden wurde. |
| [TEXT_FILE](#TEXT-FILE) | Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Textdatei verbunden wurde. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Access-Datenbank verbunden wurde.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Entspricht [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Gibt an, dass ein bestimmtes Dokument über die Office Data Source Object (ODSO)-Schnittstelle mit einer externen Datenquelle verbunden wurde.

### NONE {#NONE}
```
public static int NONE
```


Keine Seriendruck-Datenquelle ist angegeben.

### ODBC {#ODBC}
```
public static int ODBC
```


Gibt an, dass ein bestimmtes Dokument über die Open Database Connectivity-Schnittstelle mit einer externen Datenquelle verbunden wurde.

### QUERY {#QUERY}
```
public static int QUERY
```


Gibt an, dass ein bestimmtes Dokument mit einer externen Datenquelle über ein externes Abfragewerkzeug verbunden wurde.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Excel-Tabelle verbunden wurde.

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Gibt an, dass ein bestimmtes Dokument über das Dynamic Data Exchange (DDE)-System mit einer Textdatei verbunden wurde.

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
