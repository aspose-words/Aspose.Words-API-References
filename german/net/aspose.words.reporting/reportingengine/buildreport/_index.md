---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words für .NET
description: ReportingEngine BuildReport methode. Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und macht es zu einem fertigen Bericht in C#.
type: docs
weight: 40
url: /de/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und macht es zu einem fertigen Bericht.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSource | Object | Ein Datenquellenobjekt. |

### Rückgabewert

Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur sinnvoll, wenn ein Wert von[`Options`](../options/)Die Eigenschaft umfasst dieInlineErrorMessages Möglichkeit.

## Bemerkungen

Mit dieser Überladung können Sie auf die Mitglieder der Datenquelle im Vorlagendokument verweisen, Sie können jedoch nicht auf das Datenquellenobjekt selbst verweisen. Sie sollten das verwenden`BuildReport` Überlastung, um dies zu erreichen.

Ein Datenquellenobjekt kann einen der folgenden Typen haben:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Jeder andere beliebige, nicht dynamische und nicht anonyme .NET-Typ

Informationen zum Arbeiten mit Datenquellen verschiedener Typen in Vorlagendokumenten finden Sie in der Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und macht es zu einem fertigen Bericht.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSource | Object | Ein Datenquellenobjekt. |
| dataSourceName | String | Ein Name zum Verweisen auf das Datenquellenobjekt in der Vorlage. |

### Rückgabewert

Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur sinnvoll, wenn ein Wert von[`Options`](../options/)Die Eigenschaft umfasst dieInlineErrorMessages Möglichkeit.

## Bemerkungen

Mit dieser Überladung können Sie in der Vorlage auf die Mitglieder der Datenquelle und das Datenquellenobjekt selbst verweisen. Wenn Sie nicht auf das Datenquellenobjekt selbst verweisen möchten, können Sie es weglassen*dataSourceName* vorbei`Null` oder nutzen Sie die`BuildReport` Überlastung.

Ein Datenquellenobjekt kann einen der folgenden Typen haben:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Jeder andere beliebige, nicht dynamische und nicht anonyme .NET-Typ

Informationen zum Arbeiten mit Datenquellen verschiedener Typen in Vorlagendokumenten finden Sie in der Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Füllt das angegebene Vorlagendokument mit Daten aus den angegebenen Quellen und macht es zu einem fertigen Bericht.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSources | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |

### Rückgabewert

Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur sinnvoll, wenn ein Wert von[`Options`](../options/)Die Eigenschaft umfasst dieInlineErrorMessages Möglichkeit.

## Bemerkungen

Mithilfe dieser Überladung können Sie in der Vorlage auf mehrere Datenquellenobjekte und deren Mitglieder verweisen. Der Name der ersten Datenquelle kann weggelassen werden (also ein leerer String sein oder`Null`), wenn Sie auf die Mitglieder der Datenquelle verweisen, nicht jedoch auf das Datenquellenobjekt selbst. Namen der anderen Datenquellen müssen angegeben und eindeutig sein.

Wenn Sie eine einzelne Datenquelle verwenden möchten, sollten Sie die Verwendung von in Betracht ziehen`BuildReport` und`BuildReport` Überladungen stattdessen.

Ein Datenquellenobjekt kann einen der folgenden Typen haben:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Jeder andere beliebige, nicht dynamische und nicht anonyme .NET-Typ

Informationen zum Arbeiten mit Datenquellen verschiedener Typen in Vorlagendokumenten finden Sie in der Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
