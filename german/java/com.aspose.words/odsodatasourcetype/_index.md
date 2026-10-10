---
title: "OdsoDataSourceType"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO-Verbindungsinformationen in Java verbunden werden soll."
type: docs
weight: 488
url: /de/java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO-Verbindungsinformationen verbunden werden soll.

 **Remarks:** 

Die OOXML-Spezifikation ist für diese Aufzählung sehr vage. Ich vermute, sie könnte der Aufzählung WdMergeSubType entsprechen http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Gibt an, dass ein bestimmtes Dokument mit einem Adressbuch von Kontakten verbunden wurde. |
| [DATABASE](#DATABASE) | Gibt an, dass ein bestimmtes Dokument mit einer Datenbank verbunden wurde. |
| [DEFAULT](#DEFAULT) | Entspricht [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | Gibt an, dass ein bestimmtes Dokument mit einem anderen vom erzeugenden Programm unterstützten Dokumentformat verbunden wurde. |
| [DOCUMENT_2](#DOCUMENT-2) | Gibt an, dass ein bestimmtes Dokument mit einem anderen vom erzeugenden Programm unterstützten Dokumentformat verbunden wurde. |
| [EMAIL](#EMAIL) | Gibt an, dass ein bestimmtes Dokument mit einer E‑Mail-Anwendung verbunden wurde. |
| [LEGACY](#LEGACY) | Gibt an, dass ein bestimmtes Dokument mit einem veralteten Dokumentformat verbunden wurde, das vom erzeugenden Programm unterstützt wird, möglicherweise wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Gibt an, dass ein bestimmtes Dokument mit einer Datenquelle verbunden wurde, die andere Datenquellen aggregiert. |
| [NATIVE](#NATIVE) | Gibt an, dass ein bestimmtes Dokument mit einem anderen, dem erzeugenden Programm nativen Dokumentformat verbunden wurde. |
| [NONE](#NONE) | Der Typ der externen Datenquelle ist nicht angegeben. |
| [TEXT](#TEXT) | Gibt an, dass ein bestimmtes Dokument mit einer Textdatei verbunden wurde. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Gibt an, dass ein bestimmtes Dokument mit einem Adressbuch von Kontakten verbunden wurde, möglicherweise wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Gibt an, dass ein bestimmtes Dokument mit einer Datenbank verbunden wurde, möglicherweise wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Entspricht [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Gibt an, dass ein bestimmtes Dokument mit einem anderen vom erzeugenden Programm unterstützten Dokumentformat verbunden wurde, möglicherweise wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Gibt an, dass ein bestimmtes Dokument mit einem anderen vom erzeugenden Programm unterstützten Dokumentformat verbunden wurde. Möglicherweise wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Gibt an, dass ein bestimmtes Dokument mit einer E‑Mail‑Anwendung verbunden wurde. Möglicherweise wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Gibt an, dass ein bestimmtes Dokument mit einem veralteten Dokumentformat verbunden wurde, das vom erzeugenden Programm unterstützt wird, möglicherweise wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Gibt an, dass ein bestimmtes Dokument mit einer Datenquelle verbunden wurde, die andere Datenquellen aggregiert.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Gibt an, dass ein bestimmtes Dokument mit einem anderen, dem erzeugenden Programm nativen Dokumentformat verbunden wurde. Möglicherweise wdMergeSubTypeOLEDBText.

### NONE {#NONE}
```
public static int NONE
```


Der Typ der externen Datenquelle ist nicht angegeben. Möglicherweise wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


Gibt an, dass ein bestimmtes Dokument mit einer Textdatei verbunden wurde. Möglicherweise wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
