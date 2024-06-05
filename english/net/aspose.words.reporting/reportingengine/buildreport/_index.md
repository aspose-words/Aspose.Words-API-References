---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words for .NET
description: ReportingEngine BuildReport method. Populates the specified template document with data from the specified source making it a ready report in C#.
type: docs
weight: 50
url: /net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Populates the specified template document with data from the specified source making it a ready report.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | Document | A template document to be populated with data. |
| dataSource | Object | A data source object. |

### Return Value

A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [`Options`](../options/) property includes the InlineErrorMessages option.

## Remarks

Using this overload you can reference the data source's members in the template document, but you cannot reference the data source object itself. You should use the `BuildReport` overload to achieve this.

A data source object can be of one of the following types:

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
* Any other arbitrary non-dynamic and non-anonymous .NET type

For information on how to work with data sources of different types in template documents, see template syntax reference (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### See Also

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Populates the specified template document with data from the specified source making it a ready report.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | Document | A template document to be populated with data. |
| dataSource | Object | A data source object. |
| dataSourceName | String | A name to reference the data source object in the template. |

### Return Value

A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [`Options`](../options/) property includes the InlineErrorMessages option.

## Remarks

Using this overload you can reference the data source's members and the data source object itself in the template. If you are not going to reference the data source object itself, you can omit *dataSourceName* passing `null` or use the `BuildReport` overload.

A data source object can be of one of the following types:

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
* Any other arbitrary non-dynamic and non-anonymous .NET type

For information on how to work with data sources of different types in template documents, see template syntax reference (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Examples

Shows how to allow missinng members.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Shows how to remove paragraphs selectively.

```csharp
// Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Shows how to display values as dollar text.

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

### See Also

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Populates the specified template document with data from the specified sources making it a ready report.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | Document | A template document to be populated with data. |
| dataSources | Object[] | An array of data source objects. |
| dataSourceNames | String[] | An array of names to reference the data source objects within the template. |

### Return Value

A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [`Options`](../options/) property includes the InlineErrorMessages option.

## Remarks

Using this overload you can reference multiple data source objects and their members in the template. The name of the first data source can be omitted (i.e. be an empty string or `null`) if you are going to reference the data source's members but not the data source object itself. Names of the other data sources must be specified and unique.

If you are going to use a single data source, consider using of `BuildReport` and `BuildReport` overloads instead.

A data source object can be of one of the following types:

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
* Any other arbitrary non-dynamic and non-anonymous .NET type

For information on how to work with data sources of different types in template documents, see template syntax reference (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Examples

Shows how to work with charts from word 2016.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Shows how to keep inserted numbering as is.

```csharp
// By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
// With "-sourceNumbering" numbering should be separated and kept as is.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
