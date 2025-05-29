---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.Reporting.CsvDataSource 轻松访问和使用 CSV 数据。通过无缝数据集成增强您的报告！
type: docs
weight: 5410
url: /zh/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

提供对报告中使用的 CSV 文件或流的数据的访问。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class CsvDataSource
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | 使用解析 CSV 数据的默认选项，通过来自 CSV 流的数据创建新的数据源。 |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | 使用解析 CSV 数据的默认选项，利用 CSV 文件中的数据创建新的数据源。 |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | 使用指定的选项解析 CSV 数据，创建一个包含 CSV 流数据的新数据源。 |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | 使用指定的选项解析 CSV 数据，创建一个包含 CSV 文件中数据的新数据源。 |

## 评论

要在生成报告时访问相应文件或流的数据，请将此类的实例作为 数据源传递给以下之一[`ReportingEngine`](../reportingengine/).BuildReport 重载.

在模板文档中，`CsvDataSource`实例应该以与 was a 相同的方式处理DataTable 实例。有关更多信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

逗号分隔值的数据类型会根据其字符串表示形式自动确定。因此，在 template 文档中，您可以使用类型值，而不仅仅是字符串。引擎能够自动识别以下类型的 值：

* Nullable
* Nullable
* Nullable
* Nullable
* String

请注意，为了使数据类型自动识别能够正常工作，逗号分隔值的字符串表示形式应使用不变的文化设置形成。

要覆盖 CSV 数据加载的默认行为，请初始化并传递[`CsvDataLoadOptions`](../csvdataloadoptions/)实例 到此类的构造函数。

## 例子

展示如何使用 CSV 作为数据源（字符串）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
