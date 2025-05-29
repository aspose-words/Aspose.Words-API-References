---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: Aspose.Words for .NET
description: 了解 JsonDataLoadOptions 中的 SimpleValueParseMode 属性如何增强 JSON 对空值、布尔值、数字和字符串的解析。立即优化您的数据加载！
type: docs
weight: 50
url: /zh/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

获取或设置在加载 JSON 时解析 JSON 简单值（null、boolean、number、integer 和 string）的模式。此模式不会影响日期时间值的解析。默认值为 Loose.

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
```

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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
