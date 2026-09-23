---
title: "Odso"
linktitle: "Odso"
second_title: "Aspose.Words für Java"
description: "Gibt die Einstellungen des Office Data Source Object ODSO für eine Seriendruck‑Datenquelle in Java an."
type: docs
weight: 487
url: /de/java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Gibt die Einstellungen des Office Data Source Object (ODSO) für eine Seriendruck-Datenquelle an.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

ODSO scheint die "neue" Methode zu sein, die neueren Microsoft Word‑Versionen bevorzugen, wenn sie bestimmte Arten von Datenquellen für ein Seriendruckdokument angeben. ODSO erschien wahrscheinlich erstmals in Microsoft Word 2000.

Die Verwendung von ODSO ist schlecht dokumentiert und der beste Weg, zu lernen, wie die Eigenschaften dieses Objekts verwendet werden, besteht darin, ein Dokument mit einer gewünschten Datenquelle manuell in Microsoft Word zu erstellen und dieses Dokument anschließend mit Aspose.Words zu öffnen und die Eigenschaften der [Document.getMailMergeSettings()](../../com.aspose.words/document/\\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\\#setMailMergeSettings-com.aspose.words.MailMergeSettings) und [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\\#setOdso-com.aspose.words.Odso) Objekte zu untersuchen. Dies ist ein guter Ansatz, wenn Sie beispielsweise lernen möchten, wie man eine Datenquelle programmgesteuert konfiguriert.

Sie müssen normalerweise keine Objekte dieser Klasse direkt erstellen, da ODSO‑Einstellungen stets über die Eigenschaft [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\\#setOdso-com.aspose.words.Odso) verfügbar sind.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [deepClone()](#deepClone) | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [getColumnDelimiter()](#getColumnDelimiter) | Gibt das Zeichen an, das als Spaltentrennzeichen interpretiert werden soll, um Spalten in externen Datenquellen zu trennen. |
| [getDataSource()](#getDataSource) | Gibt den Speicherort der externen Datenquelle an, die mit einem Dokument verbunden werden soll, um den Seriendruck auszuführen. |
| [getDataSourceType()](#getDataSourceType) | Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO‑Verbindungsinformationen für diesen Seriendruck verbunden werden soll. |
| [getFieldMapDatas()](#getFieldMapDatas) | Ruft eine Sammlung von Objekten ab, die festlegen, wie Spalten aus der externen Datenquelle den vordefinierten Seriendruckfeldnamen im Dokument zugeordnet werden. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | Gibt an, dass eine Host‑Anwendung die erste Datenzeile in der angegebenen externen Datenquelle als Kopfzeile behandelt, die die Namen jeder Spalte in der Datenquelle enthält. |
| [getRecipientDatas()](#getRecipientDatas) | Ruft eine Sammlung von Objekten ab, die die Ein‑ bzw. Ausschließung einzelner Datensätze im Seriendruck festlegen. |
| [getTableName()](#getTableName) | Gibt den konkreten Datensatz an, mit dem eine Quelle innerhalb einer externen Datenquelle verbunden werden soll. |
| [getUdlConnectString()](#getUdlConnectString) | Gibt die Universal Data Link (UDL) Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | Gibt das Zeichen an, das als Spaltentrennzeichen interpretiert werden soll, um Spalten in externen Datenquellen zu trennen. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Gibt den Speicherort der externen Datenquelle an, die mit einem Dokument verbunden werden soll, um den Seriendruck auszuführen. |
| [setDataSourceType(int value)](#setDataSourceType-int) | Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO‑Verbindungsinformationen für diesen Seriendruck verbunden werden soll. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | Legt eine Sammlung von Objekten fest, die bestimmen, wie Spalten aus der externen Datenquelle den vordefinierten Seriendruckfeldnamen im Dokument zugeordnet werden. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | Gibt an, dass eine Host‑Anwendung die erste Datenzeile in der angegebenen externen Datenquelle als Kopfzeile behandelt, die die Namen jeder Spalte in der Datenquelle enthält. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | Legt eine Sammlung von Objekten fest, die die Ein‑ bzw. Ausschließung einzelner Datensätze im Seriendruck bestimmen. |
| [setTableName(String value)](#setTableName-java.lang.String) | Gibt den konkreten Datensatz an, mit dem eine Quelle innerhalb einer externen Datenquelle verbunden werden soll. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | Gibt die Universal Data Link (UDL) Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


Gibt eine tiefe Kopie dieses Objekts zurück.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


Gibt das Zeichen an, das als Spaltentrennzeichen interpretiert wird, das zum Trennen von Spalten in externen Datenquellen verwendet wird. Der Standardwert ist 0, was bedeutet, dass kein Spaltentrennzeichen definiert ist.

 **Remarks:** 

RK, das habe ich noch nie in Verwendung gesehen.

**Returns:**
char – Der entsprechende  char  Wert.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Gibt den Speicherort der externen Datenquelle an, die mit einem Dokument verbunden werden soll, um den Seriendruck auszuführen. Der Standardwert ist eine leere Zeichenkette.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO-Verbindungsinformationen für diesen Seriendruck verbunden werden soll. Der Standardwert ist [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Diese Einstellung ist lediglich ein Hinweis auf den Datentyp, der für diesen Seriendruck verwendet wird.

**Returns:**
int – Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der Konstanten von [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/).
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Ruft eine Sammlung von Objekten ab, die angeben, wie Spalten aus der externen Datenquelle den vordefinierten Seriendruckfeldnamen im Dokument zugeordnet werden. Dieses Objekt ist niemals null.

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


Gibt an, dass eine Host‑Anwendung die erste Datenzeile in der angegebenen externen Datenquelle als Kopfzeile behandelt, die die Namen jeder Spalte in der Datenquelle enthält. Der Standardwert ist false.

 **Remarks:** 

RK, das habe ich noch nie in Verwendung gesehen.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Ruft eine Sammlung von Objekten ab, die die Aufnahme/Ausschluss einzelner Datensätze im Seriendruck festlegen. Dieses Objekt ist niemals null.

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


Gibt den konkreten Datensatz an, mit dem eine Quelle innerhalb einer externen Datenquelle verbunden werden soll. Der Standardwert ist eine leere Zeichenkette.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


Gibt die Universal Data Link (UDL)-Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenkette.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


Gibt das Zeichen an, das als Spaltentrennzeichen interpretiert wird, das zum Trennen von Spalten in externen Datenquellen verwendet wird. Der Standardwert ist 0, was bedeutet, dass kein Spaltentrennzeichen definiert ist.

 **Remarks:** 

RK, das habe ich noch nie in Verwendung gesehen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | char | Der entsprechende  char  Wert. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Gibt den Speicherort der externen Datenquelle an, die mit einem Dokument verbunden werden soll, um den Seriendruck auszuführen. Der Standardwert ist eine leere Zeichenkette.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO-Verbindungsinformationen für diesen Seriendruck verbunden werden soll. Der Standardwert ist [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Diese Einstellung ist lediglich ein Hinweis auf den Datentyp, der für diesen Seriendruck verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der Konstanten von [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/) sein. |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Legt eine Sammlung von Objekten fest, die angeben, wie Spalten aus der externen Datenquelle den vordefinierten Seriendruckfeldnamen im Dokument zugeordnet werden. Dieses Objekt ist niemals null.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | Eine Sammlung von Objekten, die angeben, wie Spalten aus der externen Datenquelle den vordefinierten Seriendruckfeldnamen im Dokument zugeordnet werden. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Gibt an, dass eine Host‑Anwendung die erste Datenzeile in der angegebenen externen Datenquelle als Kopfzeile behandelt, die die Namen jeder Spalte in der Datenquelle enthält. Der Standardwert ist false.

 **Remarks:** 

RK, das habe ich noch nie in Verwendung gesehen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Legt eine Sammlung von Objekten fest, die die Aufnahme/Ausschluss einzelner Datensätze im Seriendruck bestimmen. Dieses Objekt ist niemals null.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | Eine Sammlung von Objekten, die die Aufnahme/Ausschluss einzelner Datensätze im Seriendruck bestimmen. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Gibt den konkreten Datensatz an, mit dem eine Quelle innerhalb einer externen Datenquelle verbunden werden soll. Der Standardwert ist eine leere Zeichenkette.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


Gibt die Universal Data Link (UDL)-Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenkette.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

