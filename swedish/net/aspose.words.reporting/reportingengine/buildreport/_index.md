---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words för .NET
description: Generera enkelt färdiga rapporter med ReportingEngines BuildReport-metod och fyll sömlöst i mallar med data från din valda källa.
type: docs
weight: 50
url: /sv/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Fyller det angivna malldokumentet med data från den angivna källan, vilket gör det till en färdig rapport.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| document | Document | Ett malldokument som ska fyllas i med data. |
| dataSource | Object | Ett datakällobjekt. |

### Returvärde

En flagga som anger om parsningen av malldokumentet lyckades. Den returnerade flaggan är endast meningsfull om ett värde för[`Options`](../options/) egenskapen inkluderar InlineErrorMessages alternativ.

## Anmärkningar

Med hjälp av denna överbelastning kan du referera till datakällans medlemmar i malldokumentet, men du kan inte referera till själva datakällobjektet. Du bör använda`BuildReport` överbelastning för att uppnå detta.

Ett datakällobjekt kan vara av en av följande typer:

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
* Annan godtycklig icke-dynamisk och icke-anonym .NET-typ

För information om hur du arbetar med datakällor av olika typer i malldokument, se referensen för mallsyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Se även

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Fyller det angivna malldokumentet med data från den angivna källan, vilket gör det till en färdig rapport.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| document | Document | Ett malldokument som ska fyllas i med data. |
| dataSource | Object | Ett datakällobjekt. |
| dataSourceName | String | Ett namn som refererar till datakällobjektet i mallen. |

### Returvärde

En flagga som anger om parsningen av malldokumentet lyckades. Den returnerade flaggan är endast meningsfull om ett värde för[`Options`](../options/) egenskapen inkluderar InlineErrorMessages alternativ.

## Anmärkningar

Med hjälp av denna överbelastning kan du referera till datakällans medlemmar och själva datakällobjektet i mallen. Om du inte ska referera till själva datakällobjektet kan du utelämna*dataSourceName* passerar`null` eller använd`BuildReport` överbelastning.

Ett datakällobjekt kan vara av en av följande typer:

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
* Annan godtycklig icke-dynamisk och icke-anonym .NET-typ

För information om hur du arbetar med datakällor av olika typer i malldokument, se referensen för mallsyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Exempel

Visar hur man tillåter saknade medlemmar.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Visar hur man tar bort stycken selektivt.

```csharp
// Mallen innehåller taggar med ett utropstecken. För sådana taggar kommer tomma stycken att tas bort.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Visar hur man visar värden som dollartext.

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

### Se även

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Fyller det angivna malldokumentet med data från de angivna källorna, vilket gör det till en färdig rapport.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| document | Document | Ett malldokument som ska fyllas i med data. |
| dataSources | Object[] | En matris med datakällobjekt. |
| dataSourceNames | String[] | En matris med namn som refererar till datakällobjekten i mallen. |

### Returvärde

En flagga som anger om parsningen av malldokumentet lyckades. Den returnerade flaggan är endast meningsfull om ett värde för[`Options`](../options/) egenskapen inkluderar InlineErrorMessages alternativ.

## Anmärkningar

Med hjälp av denna överbelastning kan du referera till flera datakällsobjekt och deras medlemmar i mallen. Namnet på den första datakällan kan utelämnas (dvs. vara en tom sträng eller`null` om du ska referera till datakällans medlemmar men inte till själva datakällobjektet. Namnen på de andra datakällorna måste anges och vara unika.

Om du ska använda en enda datakälla, överväg att använda av`BuildReport` och`BuildReport` överbelastar istället.

Ett datakällobjekt kan vara av en av följande typer:

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
* Annan godtycklig icke-dynamisk och icke-anonym .NET-typ

För information om hur du arbetar med datakällor av olika typer i malldokument, se referensen för mallsyntax (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Exempel

Visar hur man arbetar med diagram från Word 2016.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Visar hur man behåller infogad numrering som den är.

```csharp
// Som standard fortsätter numrerade listor från ett malldokument när deras identifierare matchar de från ett dokument som infogas.
// Med "-sourceNumbering" ska numrering separeras och behållas som den är.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### Se även

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
