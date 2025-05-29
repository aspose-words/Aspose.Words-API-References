---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words for .NET
description: 使用 ReportingEngine 的 BuildReport 方法轻松生成可立即使用的报告，并使用来自您选择的来源的数据无缝填充模板。
type: docs
weight: 50
url: /zh/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

使用来自指定源的数据填充指定的模板文档，使其成为一份现成的报告。

```csharp
public bool BuildReport(Document document, object dataSource)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要填充数据的模板文档。 |
| dataSource | Object | 数据源对象。 |

### 返回值

指示模板文档解析是否成功的标志。 返回的标志只有在以下情况下才有意义：[`Options`](../options/)属性包括 InlineErrorMessages选项。

## 评论

使用此重载，您可以在模板文档中引用数据源的成员，但不能 引用数据源对象本身。您应该使用`BuildReport` 重载来实现这一点。

数据源对象可以是以下类型之一：

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
* 任何其他任意非动态和非匿名 .NET 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法 参考（https://docs.aspose.com/display/wordsnet/Template+Syntax）。

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

使用来自指定源的数据填充指定的模板文档，使其成为一份现成的报告。

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要填充数据的模板文档。 |
| dataSource | Object | 数据源对象。 |
| dataSourceName | String | 用于引用模板中的数据源对象的名称。 |

### 返回值

指示模板文档解析是否成功的标志。 返回的标志只有在以下情况下才有意义：[`Options`](../options/)属性包括 InlineErrorMessages选项。

## 评论

使用此重载，您可以在模板中引用数据源的成员和数据源对象本身。 如果您不打算引用数据源对象本身，则可以省略*dataSourceName* 传球`无效的`或使用`BuildReport`超载.

数据源对象可以是以下类型之一：

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
* 任何其他任意非动态和非匿名 .NET 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法 参考（https://docs.aspose.com/display/wordsnet/Template+Syntax）。

## 例子

展示如何允许缺少成员。

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

展示如何有选择地删除段落。

```csharp
// 模板包含带有感叹号的标签。对于此类标签，空段落将被删除。
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

展示如何将值显示为美元文本。

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

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

使用来自指定来源的数据填充指定的模板文档，使其成为一份现成的报告。

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要填充数据的模板文档。 |
| dataSources | Object[] | 数据源对象数组。 |
| dataSourceNames | String[] | 用于引用模板内的数据源对象的名称数组。 |

### 返回值

指示模板文档解析是否成功的标志。 返回的标志只有在以下情况下才有意义：[`Options`](../options/)属性包括 InlineErrorMessages选项。

## 评论

使用此重载，您可以在模板中引用多个数据源对象及其成员。 第一个数据源的名称可以省略（即为空字符串或`无效的` 如果您要引用数据源的成员（而不是数据源对象本身），则必须指定其他数据源的名称（ ），并且必须唯一。

如果您要使用单一数据源，请考虑使用`BuildReport` 和`BuildReport`而是重载。

数据源对象可以是以下类型之一：

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
* 任何其他任意非动态和非匿名 .NET 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法 参考（https://docs.aspose.com/display/wordsnet/Template+Syntax）。

## 例子

展示如何使用 Word 2016 中的图表。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

显示如何保持插入的编号不变。

```csharp
// 默认情况下，当模板文档中的编号列表的标识符与插入文档中的标识符匹配时，模板文档中的编号列表将继续。
// 使用“-sourceNumbering”编号应该分开并保持原样。
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
