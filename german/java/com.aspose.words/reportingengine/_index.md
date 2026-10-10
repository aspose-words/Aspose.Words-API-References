---
title: "ReportingEngine"
linktitle: "ReportingEngine"
second_title: "Aspose.Words für Java"
description: "Stellt Routinen bereit, um Vorlagendokumente mit Daten zu füllen und eine Reihe von Einstellungen zur Steuerung dieser Routinen in Java."
type: docs
weight: 574
url: /de/java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Stellt Routinen zum Befüllen von Vorlagendokumenten mit Daten sowie eine Reihe von Einstellungen zur Steuerung dieser Routinen bereit.

Weitere Informationen finden Sie im Dokumentationsartikel zum [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und erstellt damit einen fertigen Bericht. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und erstellt damit einen fertigen Bericht. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | Füllt das angegebene Vorlagendokument mit Daten aus den angegebenen Quellen und erstellt damit einen fertigen Bericht. |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getKnownTypes()](#getKnownTypes) | Liefert ein ungeordnetes Set (d.h. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Liefert einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. |
| [getOptions()](#getOptions) | Liefert ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. |
| [getRestrictedTypes()](#getRestrictedTypes) | Gibt Typen zurück, deren Mitglieder sowie die Mitglieder abgeleiteter Typen für die Engine über die Vorlagensyntax nicht zugänglich sein sollen. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | Ermittelt einen Wert, der angibt, ob Aufrufe von benutzerdefinierten Typmitgliedern, die über die Reflexions-API durchgeführt werden, mithilfe dynamischer Klassengenerierung optimiert werden oder nicht. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Setzt einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. |
| [setOptions(int value)](#setOptions-int) | Setzt einen Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | Gibt Typen an, deren Mitglieder sowie die Mitglieder abgeleiteter Typen für die Engine über die Vorlagensyntax nicht zugänglich sein sollen. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | Setzt einen Wert, der angibt, ob Aufrufe von benutzerdefinierten Typmitgliedern, die über die Reflexions-API durchgeführt werden, mithilfe dynamischer Klassengenerierung optimiert werden oder nicht. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


Initialisiert eine neue Instanz dieser Klasse.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und erstellt damit einen fertigen Bericht.

 **Remarks:** 

Mit dieser Überladung können Sie die Mitglieder der Datenquelle im Vorlagendokument referenzieren, jedoch nicht das Datenquellenobjekt selbst. Sie sollten die Überladung [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) verwenden, um dies zu erreichen.

Ein Datenquellenobjekt kann einer der folgenden Typen sein:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Für Informationen darüber, wie man mit Datenquellen verschiedener Typen in Vorlagendokumenten arbeitet, siehe die Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSource | java.lang.Object | Ein Datenquellenobjekt. |

**Returns:**
boolean - Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur sinnvoll, wenn ein Wert der Eigenschaft [getOptions()](../../com.aspose.words/reportingengine/\\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\\#setOptions-int) die Option [ReportBuildOptions.INLINE_ERROR_MESSAGES](../../com.aspose.words/reportbuildoptions/\\#INLINE-ERROR-MESSAGES) enthält.
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und erstellt damit einen fertigen Bericht.

 **Remarks:** 

Mit dieser Überladung können Sie die Mitglieder der Datenquelle und das Datenquellenobjekt selbst in der Vorlage referenzieren. Wenn Sie das Datenquellenobjekt nicht referenzieren möchten, können Sie dataSourceName weglassen, null übergeben oder die Überladung [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\\#buildReport-com.aspose.words.Document--java.lang.Object) verwenden.

Ein Datenquellenobjekt kann einer der folgenden Typen sein:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Für Informationen darüber, wie man mit Datenquellen verschiedener Typen in Vorlagendokumenten arbeitet, siehe die Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Zeigt, wie fehlende Mitglieder erlaubt werden.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Zeigt, wie Werte als Dollar-Text angezeigt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("<<[ds.getValue1()]:dollarText>>\r<<[ds.getValue2()]:dollarText>>");

 NumericTestClass testData = new NumericTestBuilder().withValues(1234, 5621718.589).build();

 ReportingEngine report = new ReportingEngine();
 report.getKnownTypes().add(NumericTestClass.class);
 report.buildReport(doc, testData, "ds");

 doc.save(getArtifactsDir() + "ReportingEngine.DollarTextFormat.docx");
 
```

Zeigt, wie man Absätze selektiv entfernt.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSource | java.lang.Object | Ein Datenquellenobjekt. |
| dataSourceName | java.lang.String | Ein Name, um das Datenquellenobjekt in der Vorlage zu referenzieren. |

**Returns:**
boolean - Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur sinnvoll, wenn ein Wert der Eigenschaft [getOptions()](../../com.aspose.words/reportingengine/\\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\\#setOptions-int) die Option [ReportBuildOptions.INLINE_ERROR_MESSAGES](../../com.aspose.words/reportbuildoptions/\\#INLINE-ERROR-MESSAGES) enthält.
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Füllt das angegebene Vorlagendokument mit Daten aus den angegebenen Quellen und erstellt damit einen fertigen Bericht.

 **Remarks:** 

Mit dieser Überladung können Sie mehrere Datenquellenobjekte und deren Mitglieder in der Vorlage referenzieren. Der Name der ersten Datenquelle kann weggelassen werden (d. h. ein leerer String oder  null ), wenn Sie nur die Mitglieder der Datenquelle referenzieren möchten, nicht das Datenquellenobjekt selbst. Die Namen der anderen Datenquellen müssen angegeben und eindeutig sein.

Wenn Sie eine einzelne Datenquelle verwenden möchten, sollten Sie stattdessen die Überladungen von [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) und [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) verwenden.

Ein Datenquellenobjekt kann einer der folgenden Typen sein:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Für Informationen darüber, wie man mit Datenquellen verschiedener Typen in Vorlagendokumenten arbeitet, siehe die Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Zeigt, wie eingefügte Nummerierung unverändert beibehalten wird.

```

 // By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
 // With "-sourceNumbering" numbering should be separated and kept as is.
 Document template = DocumentHelper.createSimpleDocument("<>" + System.lineSeparator() + "<>");

 DocumentTestClass doc = new DocumentTestBuilder()
         .withDocument(new Document(getMyDir() + "List item.docx")).build();

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.REMOVE_EMPTY_PARAGRAPHS); }
 engine.buildReport(template, new Object[] { doc }, new String[] { "src" });

 template.save(getArtifactsDir() + "ReportingEngine.SourseListNumbering.docx");
 
```

Zeigt, wie man mit Diagrammen aus Word 2016 arbeitet.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSources | java.lang.Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | java.lang.String[] | Ein Array von Namen, um die Datenquellenobjekte innerhalb der Vorlage zu referenzieren. |

**Returns:**
boolean - Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur sinnvoll, wenn ein Wert der Eigenschaft [getOptions()](../../com.aspose.words/reportingengine/\\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\\#setOptions-int) die Option [ReportBuildOptions.INLINE_ERROR_MESSAGES](../../com.aspose.words/reportbuildoptions/\\#INLINE-ERROR-MESSAGES) enthält.
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Liefert ein ungeordnetes Set (d.h. eine Sammlung eindeutiger Elemente), das java.lang.Class-Objekte enthält, deren vollständig oder teilweise qualifizierte Namen innerhalb von Berichtsvorlagen, die von dieser Engine-Instanz verarbeitet werden, verwendet werden können, um die statischen Mitglieder der entsprechenden Typen aufzurufen, Typumwandlungen durchzuführen usw.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Liefert einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. Der Standardwert ist eine leere Zeichenkette.

 **Remarks:** 

Die Eigenschaft sollte zusammen mit der Option [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) verwendet werden. Andernfalls wird eine Ausnahme ausgelöst, wenn ein fehlendes Mitglied eines Objekts gefunden wird.

Die Eigenschaft wirkt sich nur auf die Ausgabe eines Template-Ausdrucks aus, der eine einfache Referenz auf ein fehlendes Objektmitglied darstellt. Zum Beispiel wird die Ausgabe eines binären Operators, bei dem einer der Operanden auf ein fehlendes Objektmitglied verweist, nicht beeinflusst.

Der Wert dieser Eigenschaft kann nicht auf null gesetzt werden.

 **Examples:** 

Zeigt, wie fehlende Mitglieder erlaubt werden.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Returns:**
java.lang.String – Ein Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt.
### getOptions() {#getOptions}
```
public int getOptions()
```


Liefert ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern.

 **Examples:** 

Zeigt, wie fehlende Mitglieder erlaubt werden.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Zeigt, wie Optionen für die Reporting Engine festgelegt werden.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Returns:**
int – Ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. Der zurückgegebene Wert ist eine bitweise Kombination von [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/)‑Konstanten.
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


Gibt Typen zurück, deren Mitglieder sowie die Mitglieder abgeleiteter Typen für die Engine über die Vorlagensyntax nicht zugänglich sein sollen.

 **Remarks:** 

Das zurückgegebene Array enthält Elemente, die zuvor mit [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) festgelegt wurden.

Das Ändern von Elementen des zurückgegebenen Arrays hat keinen Einfluss auf eingeschränkte Typen. Um eingeschränkte Typen zu ändern, verwenden Sie stattdessen [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class).

**Returns:**
java.lang.Class[] – Typen, deren Mitglieder sowie die Mitglieder abgeleiteter Typen für die Engine über die Vorlagensyntax unzugänglich sein sollen.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


Gibt einen Wert zurück, der angibt, ob Aufrufe von benutzerdefinierten Typmitgliedern, die über die Reflexions‑API durchgeführt werden, mittels dynamischer Klassengenerierung optimiert werden oder nicht. Der Standardwert ist  true .

 **Remarks:** 

Es gibt einige Szenarien, in denen es vorzuziehen ist, diese Optimierung zu deaktivieren. Zum Beispiel, wenn Sie ständig mit kleinen Sammlungen von Datenobjekten arbeiten, kann der Aufwand für die dynamische Klassengenerierung stärker auffallen als der Aufwand für direkte Reflexions‑API‑Aufrufe. Die Option hat keine Wirkung, wenn sie unter iOS ausgeführt wird und die Reflexionsoptimierung nicht verwendet wird.

**Returns:**
boolean – Ein Wert, der angibt, ob Aufrufe von benutzerdefinierten Typmitgliedern, die über die Reflexions‑API durchgeführt werden, mittels dynamischer Klassengenerierung optimiert werden oder nicht.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Setzt einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. Der Standardwert ist eine leere Zeichenkette.

 **Remarks:** 

Die Eigenschaft sollte zusammen mit der Option [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) verwendet werden. Andernfalls wird eine Ausnahme ausgelöst, wenn ein fehlendes Mitglied eines Objekts gefunden wird.

Die Eigenschaft wirkt sich nur auf die Ausgabe eines Template-Ausdrucks aus, der eine einfache Referenz auf ein fehlendes Objektmitglied darstellt. Zum Beispiel wird die Ausgabe eines binären Operators, bei dem einer der Operanden auf ein fehlendes Objektmitglied verweist, nicht beeinflusst.

Der Wert dieser Eigenschaft kann nicht auf null gesetzt werden.

 **Examples:** 

Zeigt, wie fehlende Mitglieder erlaubt werden.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Setzt einen Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern.

 **Examples:** 

Zeigt, wie fehlende Mitglieder erlaubt werden.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Zeigt, wie Optionen für die Reporting Engine festgelegt werden.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. Der Wert muss eine bitweise Kombination von [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/)‑Konstanten sein. |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


Gibt Typen an, deren Mitglieder sowie die Mitglieder abgeleiteter Typen für die Engine über die Vorlagensyntax nicht zugänglich sein sollen.

 **Remarks:** 

Eingeschränkte Typen sollten vor dem allerersten Erstellen eines Berichts festgelegt werden. Nachdem  BuildReportbuildReport  aufgerufen wurde, können eingeschränkte Typen nicht mehr geändert werden und bei einem Versuch, dies zu tun, wird eine Ausnahme ausgelöst. Der beste Zeitpunkt, um eingeschränkte Typen festzulegen, ist beim Anwendungsstart.

Beachten Sie, dass eine große Anzahl eingeschränkter Typen die Leistung beeinträchtigen kann, daher ist es besser, nur jene Typen zu beschränken, deren Mitgliederzugriff wirklich sensibel ist.

Wirft java.lang.IllegalArgumentException in den folgenden Fällen:

\-  types  ist null.

\- Einer der  types  Elemente ist  null .

\- Einer der Typen‑Elemente stellt einen unsichtbaren Typ dar, d. h. einen nicht‑öffentlichen Typ oder einen öffentlichen verschachtelten Typ, dessen äußerer Typ nicht‑öffentlich ist.

\- Einer der Typen‑Elemente stellt einen Array‑Typ dar.

\- Typen enthalten doppelte Einträge.

 **Examples:** 

Zeigt, wie der Zugriff auf Mitglieder von als unsicher eingestuften Typen verweigert wird.

```

 Document doc =
         DocumentHelper.createSimpleDocument(
                 "<><<[typeVar]>>");

 // Note, that you can't set restricted types during or after building a report.
 ReportingEngine.setRestrictedTypes(Class.class);
 // We set "AllowMissingMembers" option to avoid exceptions during building a report.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
 engine.buildReport(doc, new Object());

 // We get an empty string because we can't access the GetType() method.
 Assert.assertEquals(doc.getText().trim(), "");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Typen | java.lang.Class[] | Typen, die eingeschränkt werden sollen. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


Legt einen Wert fest, der angibt, ob Aufrufe von benutzerdefinierten Typenmitgliedern, die über die Reflexions‑API durchgeführt werden, mittels dynamischer Klassengenerierung optimiert werden oder nicht. Der Standardwert ist true.

 **Remarks:** 

Es gibt einige Szenarien, in denen es vorzuziehen ist, diese Optimierung zu deaktivieren. Zum Beispiel, wenn Sie ständig mit kleinen Sammlungen von Datenobjekten arbeiten, kann der Aufwand für die dynamische Klassengenerierung stärker auffallen als der Aufwand für direkte Reflexions‑API‑Aufrufe. Die Option hat keine Wirkung, wenn sie unter iOS ausgeführt wird und die Reflexionsoptimierung nicht verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob Aufrufe von benutzerdefinierten Typenmitgliedern, die über die Reflexions‑API durchgeführt werden, mittels dynamischer Klassengenerierung optimiert werden oder nicht. |

