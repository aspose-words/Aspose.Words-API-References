---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words for .NET
description: 使用 JsonDataSource 构造函数轻松创建强大的数据源，实现 JSON 文件的无缝集成和优化的数据解析。
type: docs
weight: 10
url: /zh/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

使用解析 JSON 数据的默认选项，使用来自 JSON 文件的数据创建新的数据源。

```csharp
public JsonDataSource(string jsonPath)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonPath | String | 用作数据源的 JSON 文件的路径。 |

### 也可以看看

* class [JsonDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

使用解析 JSON 数据的默认选项，创建一个包含 JSON 流数据的新数据源。

```csharp
public JsonDataSource(Stream jsonStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonStream | Stream | 用作数据源的 JSON 数据流。 |

### 也可以看看

* class [JsonDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

使用指定的选项解析 JSON 数据，创建一个包含 JSON 文件中数据的新数据源。

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonPath | String | 用作数据源的 JSON 文件的路径。 |
| options | JsonDataLoadOptions | 解析 JSON 数据的选项。 |

## 例子

展示如何使用 JSON 作为数据源（字符串）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### 也可以看看

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

使用指定的选项解析 JSON 数据，创建一个包含 JSON 流数据的新数据源。

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonStream | Stream | 用作数据源的 JSON 数据流。 |
| options | JsonDataLoadOptions | 解析 JSON 数据的选项。 |

## 例子

展示如何使用 JSON 作为数据源（流）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"}
};

using (FileStream stream = File.OpenRead(MyDir + "List of people.json"))
{
    JsonDataSource dataSource = new JsonDataSource(stream, options);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataStream.docx");
```

### 也可以看看

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
