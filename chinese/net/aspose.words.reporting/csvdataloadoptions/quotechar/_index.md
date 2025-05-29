---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: Aspose.Words for .NET
description: 发现 CsvDataLoadOptions QuoteChar 属性，轻松自定义字段值引用，实现无缝数据处理和改进的 CSV 管理。
type: docs
weight: 50
url: /zh/net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

获取或设置用于引用字段值的字符。

```csharp
public char QuoteChar { get; set; }
```

## 评论

默认值为“”（引号）。

将字符加倍以将其放入引用文本中。

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

* class [CsvDataLoadOptions](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
