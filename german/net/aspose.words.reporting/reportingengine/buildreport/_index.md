---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos gebrauchsfertige Berichte mit der BuildReport-Methode von ReportingEngine und füllen Sie Vorlagen nahtlos mit Daten aus der von Ihnen gewählten Quelle.
type: docs
weight: 50
url: /de/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und macht daraus einen fertigen Bericht.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSource | Object | Ein Datenquellenobjekt. |

### Rückgabewert

Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur dann sinnvoll, wenn ein Wert des[`Options`](../options/) Eigenschaft enthält dieInlineErrorMessages Option.

## Bemerkungen

Mit dieser Überladung können Sie die Elemente der Datenquelle im Vorlagendokument referenzieren, aber nicht auf das Datenquellenobjekt selbst. Sie sollten die`BuildReport` Überladung, um dies zu erreichen.

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
* Jeder andere beliebige nicht dynamische und nicht anonyme .NET-Typ

Informationen zum Arbeiten mit Datenquellen unterschiedlichen Typs in Vorlagendokumenten finden Sie in der Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und macht daraus einen fertigen Bericht.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSource | Object | Ein Datenquellenobjekt. |
| dataSourceName | String | Ein Name zum Verweisen auf das Datenquellenobjekt in der Vorlage. |

### Rückgabewert

Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur dann sinnvoll, wenn ein Wert des[`Options`](../options/) Eigenschaft enthält dieInlineErrorMessages Option.

## Bemerkungen

Mit dieser Überladung können Sie in der Vorlage auf die Mitglieder der Datenquelle und das Datenquellenobjekt selbst verweisen. Wenn Sie nicht auf das Datenquellenobjekt selbst verweisen, können Sie Folgendes weglassen:*dataSourceName* vorbei`null` oder verwenden Sie die`BuildReport` Überlastung.

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
* Jeder andere beliebige nicht dynamische und nicht anonyme .NET-Typ

Informationen zum Arbeiten mit Datenquellen unterschiedlichen Typs in Vorlagendokumenten finden Sie in der Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Beispiele

Zeigt, wie fehlende Mitglieder zugelassen werden.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Zeigt, wie Absätze selektiv entfernt werden.

```csharp
// Die Vorlage enthält Tags mit einem Ausrufezeichen. Bei solchen Tags werden leere Absätze entfernt.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Zeigt, wie Werte als Dollartext angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("<<[ds.Value1]:dollarText>>\r<<[ds.Value2]:dollarText>>");

NumericTestClass testData = new NumericTestBuilder().WithValues(1234, 5621718.589).Build();

ReportingEngine report = new ReportingEngine();
report.KnownTypes.Add(typeof(NumericTestClass));
report.BuildReport(doc, testData, "ds");

doc.Save(ArtifactsDir + "ReportingEngine.DollarTextFormat.docx");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Füllt das angegebene Vorlagendokument mit Daten aus den angegebenen Quellen und macht daraus einen fertigen Bericht.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Ein Vorlagendokument, das mit Daten gefüllt werden soll. |
| dataSources | Object[] | Ein Array von Datenquellenobjekten. |
| dataSourceNames | String[] | Ein Array von Namen zum Verweisen auf die Datenquellenobjekte innerhalb der Vorlage. |

### Rückgabewert

Ein Flag, das angibt, ob das Parsen des Vorlagendokuments erfolgreich war. Das zurückgegebene Flag ist nur dann sinnvoll, wenn ein Wert des[`Options`](../options/) Eigenschaft enthält dieInlineErrorMessages Option.

## Bemerkungen

Mit dieser Überladung können Sie mehrere Datenquellenobjekte und deren Mitglieder in der Vorlage referenzieren. Der Name der ersten Datenquelle kann weggelassen werden (d. h. eine leere Zeichenfolge sein oder`null`), wenn Sie auf die Mitglieder der Datenquelle verweisen, nicht aber auf das Datenquellenobjekt selbst. Die Namen der anderen Datenquellen müssen angegeben und eindeutig sein.

Wenn Sie eine einzelne Datenquelle verwenden, sollten Sie die Verwendung von`BuildReport` und`BuildReport` stattdessen Überladungen.

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
* Jeder andere beliebige nicht dynamische und nicht anonyme .NET-Typ

Informationen zum Arbeiten mit Datenquellen unterschiedlichen Typs in Vorlagendokumenten finden Sie in der Referenz zur Vorlagensyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Beispiele

Zeigt, wie man mit Diagrammen aus Word 2016 arbeitet.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Zeigt, wie die eingefügte Nummerierung unverändert bleibt.

```csharp
// Standardmäßig werden nummerierte Listen aus einem Vorlagendokument fortgesetzt, wenn ihre Bezeichner mit denen aus einem eingefügten Dokument übereinstimmen.
// Mit „-sourceNumbering“ soll die Nummerierung getrennt und so belassen werden, wie sie ist.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
