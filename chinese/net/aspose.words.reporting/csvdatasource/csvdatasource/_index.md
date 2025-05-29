---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words for .NET
description: 使用我们的 CsvDataSource 构造函数轻松创建强大的 CSV 数据源。使用默认选项简化数据解析，实现无缝集成。
type: docs
weight: 10
url: /zh/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

使用解析 CSV 数据的默认选项，利用 CSV 文件中的数据创建新的数据源。

```csharp
public CsvDataSource(string csvPath)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvPath | String | 用作数据源的 CSV 文件的路径。 |

### 也可以看看

* class [CsvDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

使用指定的选项解析 CSV 数据，创建一个包含 CSV 文件中数据的新数据源。

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvPath | String | 用作数据源的 CSV 文件的路径。 |
| options | CsvDataLoadOptions | 解析 CSV 数据的选项。 |

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

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

使用解析 CSV 数据的默认选项，通过来自 CSV 流的数据创建新的数据源。

```csharp
public CsvDataSource(Stream csvStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvStream | Stream | 用作数据源的 CSV 数据流。 |

### 也可以看看

* class [CsvDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

使用指定的选项解析 CSV 数据，创建一个包含 CSV 流数据的新数据源。

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvStream | Stream | 用作数据源的 CSV 数据流。 |
| options | CsvDataLoadOptions | 解析 CSV 数据的选项。 |

## 例子

展示如何使用 CSV 作为数据源（流）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### 也可以看看

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
