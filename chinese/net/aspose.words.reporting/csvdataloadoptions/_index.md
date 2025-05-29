---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Reporting.CsvDataLoadOptions，实现高效的 CSV 数据解析。立即使用可自定义的选项优化您的文档处理！
type: docs
weight: 5400
url: /zh/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

表示解析 CSV 数据的选项。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class CsvDataLoadOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | 使用默认选项初始化此类的新实例。 |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | 初始化此类的新实例，并指定 CSV 数据是否在第一行包含列名 。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | 获取或设置用于注释 CSV 数据行的字符。 |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | 获取或设置用作列分隔符的字符。 |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | 获取或设置一个值，指示 CSV 数据的第一条记录是否包含列名。 |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | 获取或设置用于引用字段值的字符。 |

## 评论

此类的实例可以传递到[`CsvDataSource`](../csvdatasource/).

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
