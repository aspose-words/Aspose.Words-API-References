---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words for .NET
description: 探索 JsonDataLoadOptions 的 ExactDateTimeParseFormats，实现精准的 JSON 日期时间解析。轻松自定义格式，实现无缝数据加载！
type: docs
weight: 30
url: /zh/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

获取或设置在加载 JSON 时解析 JSON 日期时间值的精确格式。默认值为`无效的`.

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## 评论

使用 Microsoft® JSON 日期时间格式编码的字符串（例如，“/Date(1224043200000)/”）始终被 识别为日期时间值，无论此属性的值如何。该属性定义了在解析字符串中的日期时间值时要使用的其他 格式，如下所示：

* 当`ExactDateTimeParseFormats`是`无效的` 、ISO-8601 格式以及当前、美国英语和新西兰英语文化支持的所有日期时间格式均按上述顺序额外使用。
* 当`ExactDateTimeParseFormats`包含字符串，它们用作利用当前文化的附加日期时间 格式。
* 当`ExactDateTimeParseFormats`为空，不使用任何其他日期时间格式。

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

* class [JsonDataLoadOptions](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
