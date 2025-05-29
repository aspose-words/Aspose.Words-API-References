---
title: CsvDataLoadOptions.HasHeaders
linktitle: HasHeaders
articleTitle: HasHeaders
second_title: Aspose.Words for .NET
description: 发现 CsvDataLoadOptions 的 HasHeaders 属性，通过指定第一条记录是否包含列名来实现无缝数据集成，从而轻松管理 CSV 导入。
type: docs
weight: 40
url: /zh/net/aspose.words.reporting/csvdataloadoptions/hasheaders/
---
## CsvDataLoadOptions.HasHeaders property

获取或设置一个值，指示 CSV 数据的第一条记录是否包含列名。

```csharp
public bool HasHeaders { get; set; }
```

## 评论

默认值为`错误的`.

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
