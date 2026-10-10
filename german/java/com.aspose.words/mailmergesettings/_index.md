---
title: "MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words für Java"
description: "Gibt alle Mail-Merge-Informationen für ein Dokument in Java an."
type: docs
weight: 445
url: /de/java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Gibt alle Seriendruckinformationen für ein Dokument an.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Sie können dieses Objekt verwenden, um eine Mail-Merge-Datenquelle für ein Dokument anzugeben, und diese Informationen (zusammen mit den verfügbaren Datenfeldern) werden in Microsoft Word angezeigt, wenn der Benutzer dieses Dokument öffnet. Oder Sie können dieses Objekt verwenden, um die Mail-Merge-Einstellungen abzufragen, die der Benutzer in Microsoft Word für dieses Dokument festgelegt hat.

Sie müssen normalerweise keine Objekte dieser Klasse direkt erstellen, da die Mail-Merge-Einstellungen eines Dokuments stets über die Eigenschaft [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) verfügbar sind.

Um festzustellen, ob dieses Dokument ein Haupt‑Mail‑Merge‑Dokument ist, prüfen Sie den Wert der Eigenschaft [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int).

Um Mail‑Merge‑Einstellungen und Datenquelleninformationen aus einem Dokument zu entfernen, können Sie die Methode [clear()](../../com.aspose.words/mailmergesettings/\#clear) verwenden. Aspose.Words schreibt keine Mail‑Merge‑Einstellungen in ein Dokument, wenn die Eigenschaft [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) auf [MailMergeMainDocumentType.NOT\_A\_MERGE\_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/\#NOT-A-MERGE-DOCUMENT) gesetzt ist oder die Eigenschaft [getDataType()](../../com.aspose.words/mailmergesettings/\#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/\#setDataType-int) auf [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/\#NONE) gesetzt ist.

Der beste Weg, um zu lernen, wie man die Eigenschaften dieses Objekts verwendet, besteht darin, manuell in Microsoft Word ein Dokument mit einer gewünschten Datenquelle zu erstellen und dann dieses Dokument mit Aspose.Words zu öffnen und die Eigenschaften der [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) und [getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) Objekte zu untersuchen. Dies ist ein guter Ansatz, wenn Sie beispielsweise lernen möchten, wie man eine Datenquelle programmgesteuert konfiguriert.

Aspose.Words bewahrt Mail-Merge-Informationen beim Laden, Speichern und Konvertieren von Dokumenten zwischen verschiedenen Formaten, verwendet diese Informationen jedoch nicht, wenn es sein eigenes Mail-Merge mit dem [MailMerge](../../com.aspose.words/mailmerge/) Objekt durchführt.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clear()](#clear) | Löscht die Mail-Merge-Einstellungen so, dass beim Speichern des Dokuments keine Mail-Merge-Einstellungen gespeichert werden und es zu einem normalen Dokument wird. |
| [deepClone()](#deepClone) | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [getActiveRecord()](#getActiveRecord) | Gibt den einsbasierten Index des Datensatzes aus der Datenquelle an, der in Microsoft Word angezeigt werden soll. |
| [getAddressFieldName()](#getAddressFieldName) | Gibt die Spalte in der Datenquelle an, die E‑Mail‑Adressen enthält. |
| [getCheckErrors()](#getCheckErrors) | Gibt den Typ der Fehlermeldung an, die von Microsoft Word beim Durchführen eines Mail-Merge ausgegeben werden soll. |
| [getConnectString()](#getConnectString) | Gibt die Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. |
| [getDataSource()](#getDataSource) | Gibt den Pfad zur Mail-Merge-Datenquelle an. |
| [getDataType()](#getDataType) | Gibt den Typ der Mail-Merge-Datenquelle und die Methode des Datenzugriffs an. |
| [getDestination()](#getDestination) | Gibt an, wie Microsoft Word die Ergebnisse eines Mail-Merge ausgibt. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | Gibt an, wie eine Anwendung, die das Mail-Merge durchführt, mit Leerzeilen in den aus dem Mail-Merge resultierenden zusammengeführten Dokumenten umgehen soll. |
| [getHeaderSource()](#getHeaderSource) | Gibt den Pfad zur Mail-Merge-Header-Quelle an. |
| [getLinkToQuery()](#getLinkToQuery) | Nicht sicher bei diesem. |
| [getMailAsAttachment()](#getMailAsAttachment) | Gibt an, dass die während eines Mail-Merge-Vorgangs erzeugten Dokumente als Anhang per E‑Mail gesendet werden sollen, anstatt im eigentlichen E‑Mail-Textkörper. |
| [getMailSubject()](#getMailSubject) | Gibt den Text an, der in der Betreffzeile der während des Mail-Merge erzeugten E‑Mails oder Faxe erscheinen soll. |
| [getMainDocumentType()](#getMainDocumentType) | Gibt den Hauptdokumenttyp des Mail-Merge an. |
| [getOdso()](#getOdso) | Ruft das Objekt ab, das die Einstellungen des Office Data Source Object (ODSO) spezifiziert. |
| [getQuery()](#getQuery) | Enthält die Structured Query Language‑Zeichenfolge, die gegen die angegebene externe Datenquelle ausgeführt wird, um den Satz von Datensätzen zurückzugeben, die beim Durchführen des Mail-Merge in das Dokument importiert werden sollen. |
| [getViewMergedData()](#getViewMergedData) | Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle anzeigen soll, wo Zusammenführungsfelder eingefügt wurden (z. B. |
| [setActiveRecord(int value)](#setActiveRecord-int) | Gibt den einsbasierten Index des Datensatzes aus der Datenquelle an, der in Microsoft Word angezeigt werden soll. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | Gibt die Spalte in der Datenquelle an, die E‑Mail‑Adressen enthält. |
| [setCheckErrors(int value)](#setCheckErrors-int) | Gibt den Typ der Fehlermeldung an, die von Microsoft Word beim Durchführen eines Mail-Merge ausgegeben werden soll. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | Gibt die Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Gibt den Pfad zur Mail-Merge-Datenquelle an. |
| [setDataType(int value)](#setDataType-int) | Gibt den Typ der Mail-Merge-Datenquelle und die Methode des Datenzugriffs an. |
| [setDestination(int value)](#setDestination-int) | Gibt an, wie Microsoft Word die Ergebnisse eines Mail-Merge ausgibt. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | Gibt an, wie eine Anwendung, die das Mail-Merge durchführt, mit Leerzeilen in den aus dem Mail-Merge resultierenden zusammengeführten Dokumenten umgehen soll. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | Gibt den Pfad zur Mail-Merge-Header-Quelle an. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | Nicht sicher bei diesem. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | Gibt an, dass die während eines Mail-Merge-Vorgangs erzeugten Dokumente als Anhang per E‑Mail gesendet werden sollen, anstatt im eigentlichen E‑Mail-Textkörper. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | Gibt den Text an, der in der Betreffzeile der während des Mail-Merge erzeugten E‑Mails oder Faxe erscheinen soll. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | Gibt den Hauptdokumenttyp des Mail-Merge an. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | Setzt das Objekt, das die Einstellungen des Office Data Source Object (ODSO) spezifiziert. |
| [setQuery(String value)](#setQuery-java.lang.String) | Enthält die Structured Query Language‑Zeichenfolge, die gegen die angegebene externe Datenquelle ausgeführt wird, um den Satz von Datensätzen zurückzugeben, die beim Durchführen des Mail-Merge in das Dokument importiert werden sollen. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle anzeigen soll, wo Zusammenführungsfelder eingefügt wurden (z. B. |
### clear() {#clear}
```
public void clear()
```


Löscht die Mail-Merge-Einstellungen so, dass beim Speichern des Dokuments keine Mail-Merge-Einstellungen gespeichert werden und es zu einem normalen Dokument wird.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


Gibt eine tiefe Kopie dieses Objekts zurück.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


Gibt den einsbasierten Index des Datensatzes aus der Datenquelle an, der in Microsoft Word angezeigt werden soll. Der Standardwert ist 1.

**Returns:**
int - Der entsprechende int-Wert.
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


Gibt die Spalte in der Datenquelle an, die E‑Mail‑Adressen enthält. Der Standardwert ist eine leere Zeichenfolge.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


Gibt den Typ der Fehlermeldung an, die von Microsoft Word beim Durchführen eines Seriendrucks durchgeführt werden soll. Der Standardwert ist [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/).
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


Gibt die Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenfolge.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Gibt den Pfad zur Seriendruck‑Datenquelle an. Der Standardwert ist eine leere Zeichenfolge.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getDataType() {#getDataType}
```
public int getDataType()
```


Gibt den Typ der Seriendruck‑Datenquelle und die Methode des Datenzugriffs an. Der Standardwert ist [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [MailMergeDataType](../../com.aspose.words/mailmergedatatype/).
### getDestination() {#getDestination}
```
public int getDestination()
```


Gibt an, wie Microsoft Word die Ergebnisse eines Seriendrucks ausgibt. Der Standardwert ist [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [MailMergeDestination](../../com.aspose.words/mailmergedestination/).
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


Gibt an, wie eine Anwendung, die den Seriendruck ausführt, mit Leerzeilen in den aus dem Seriendruck resultierenden Dokumenten umgehen soll. Der Standardwert ist false.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


Gibt den Pfad zur Seriendruck‑Header‑Quelle an. Der Standardwert ist eine leere Zeichenfolge.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


Unsicher bei diesem. Die Microsoft Word Automation Reference legt nahe, dass dies angibt, dass die Abfrage jedes Mal ausgeführt wird, wenn das Dokument in Microsoft Word geöffnet wird. Die OOXML‑Spezifikation hingegen legt nahe, dass dies angibt, dass die Abfrage einen Verweis auf eine externe Abfragedatei enthält, die die eigentliche Abfrage enthält. Der Standardwert ist false.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


Gibt an, dass die während eines Seriendruckvorgangs erzeugten Dokumente als Anhang per E‑Mail gesendet werden sollen, anstatt im eigentlichen E‑Mail‑Textkörper. Der Standardwert ist false.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


Gibt den Text an, der in der Betreffzeile der während des Seriendrucks erzeugten E‑Mails oder Faxe erscheinen soll. Der Standardwert ist eine leere Zeichenfolge.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


Gibt den Typ des Seriendruck‑Hauptdokuments an. Der Standardwert ist [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Das Hauptdokument ist das Dokument, das Informationen enthält, die für jede Version des zusammengeführten Dokuments gleich sind.

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/).
### getOdso() {#getOdso}
```
public Odso getOdso()
```


Ruft das Objekt ab, das die Einstellungen des Office Data Source Object (ODSO) spezifiziert.

 **Remarks:** 

Dieses Objekt ist niemals null.

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


Enthält die Structured Query Language‑Zeichenfolge, die gegen die angegebene externe Datenquelle ausgeführt werden soll, um den Datensatz zurückzugeben, der beim Durchführen des Seriendrucks in das Dokument importiert wird. Der Standardwert ist eine leere Zeichenfolge.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle anzeigen soll, in der Zusammenführungsfelder eingefügt wurden (z. B. zusammengeführte Daten in der Vorschau). Der Standardwert ist false.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


Gibt den einsbasierten Index des Datensatzes aus der Datenquelle an, der in Microsoft Word angezeigt werden soll. Der Standardwert ist 1.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


Gibt die Spalte in der Datenquelle an, die E‑Mail‑Adressen enthält. Der Standardwert ist eine leere Zeichenfolge.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


Gibt den Typ der Fehlermeldung an, die von Microsoft Word beim Durchführen eines Seriendrucks durchgeführt werden soll. Der Standardwert ist [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int-Wert. Der Wert muss einer der Konstanten von [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/) sein. |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


Gibt die Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenfolge.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Gibt den Pfad zur Seriendruck‑Datenquelle an. Der Standardwert ist eine leere Zeichenfolge.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


Gibt den Typ der Seriendruck‑Datenquelle und die Methode des Datenzugriffs an. Der Standardwert ist [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int-Wert. Der Wert muss einer der Konstanten von [MailMergeDataType](../../com.aspose.words/mailmergedatatype/) sein. |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


Gibt an, wie Microsoft Word die Ergebnisse eines Seriendrucks ausgibt. Der Standardwert ist [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int-Wert. Der Wert muss einer der Konstanten von [MailMergeDestination](../../com.aspose.words/mailmergedestination/) sein. |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


Gibt an, wie eine Anwendung, die den Seriendruck ausführt, mit Leerzeilen in den aus dem Seriendruck resultierenden Dokumenten umgehen soll. Der Standardwert ist false.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


Gibt den Pfad zur Seriendruck‑Header‑Quelle an. Der Standardwert ist eine leere Zeichenfolge.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


Unsicher bei diesem. Die Microsoft Word Automation Reference legt nahe, dass dies angibt, dass die Abfrage jedes Mal ausgeführt wird, wenn das Dokument in Microsoft Word geöffnet wird. Die OOXML‑Spezifikation hingegen legt nahe, dass dies angibt, dass die Abfrage einen Verweis auf eine externe Abfragedatei enthält, die die eigentliche Abfrage enthält. Der Standardwert ist false.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


Gibt an, dass die während eines Seriendruckvorgangs erzeugten Dokumente als Anhang per E‑Mail gesendet werden sollen, anstatt im eigentlichen E‑Mail‑Textkörper. Der Standardwert ist false.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


Gibt den Text an, der in der Betreffzeile der während des Seriendrucks erzeugten E‑Mails oder Faxe erscheinen soll. Der Standardwert ist eine leere Zeichenfolge.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


Gibt den Typ des Seriendruck‑Hauptdokuments an. Der Standardwert ist [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Das Hauptdokument ist das Dokument, das Informationen enthält, die für jede Version des zusammengeführten Dokuments gleich sind.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int-Wert. Der Wert muss einer der Konstanten von [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/) sein. |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


Setzt das Objekt, das die Einstellungen des Office Data Source Object (ODSO) spezifiziert.

 **Remarks:** 

Dieses Objekt ist niemals null.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | Das Objekt, das die Einstellungen des Office Data Source Object (ODSO) festlegt. |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Enthält die Structured Query Language‑Zeichenfolge, die gegen die angegebene externe Datenquelle ausgeführt werden soll, um den Datensatz zurückzugeben, der beim Durchführen des Seriendrucks in das Dokument importiert wird. Der Standardwert ist eine leere Zeichenfolge.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle anzeigen soll, in der Zusammenführungsfelder eingefügt wurden (z. B. zusammengeführte Daten in der Vorschau). Der Standardwert ist false.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

