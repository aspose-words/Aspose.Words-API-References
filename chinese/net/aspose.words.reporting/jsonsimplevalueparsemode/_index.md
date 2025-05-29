---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Reporting.JsonSimpleValueParseMode 枚举，实现高效的 JSON 解析。轻松无缝处理空值、布尔值、数字和字符串！
type: docs
weight: 5440
url: /zh/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

指定加载 JSON 时解析 JSON 简单值（null、boolean、number、integer 和 string）的模式。 此模式不会影响日期时间值的解析。

```csharp
public enum JsonSimpleValueParseMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Loose | `0` | 指定在解析 JSON 简单值的字符串表示形式时确定其类型的模式。 例如，在此模式下，JSON 代码片段“{prop：“123”}”中的“prop”类型被确定为整数。 |
| Strict | `1` | 指定从 JSON 符号本身确定 JSON 简单值类型的模式。 例如，在此模式下，JSON 代码片段“{prop：“123”}”中的“prop”类型被确定为字符串。 |

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

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
