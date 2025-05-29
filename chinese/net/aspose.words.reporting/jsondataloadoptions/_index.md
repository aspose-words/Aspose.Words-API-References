---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Reporting.JsonDataLoadOptions 类，实现无缝 JSON 数据解析。使用灵活的选项增强您的文档处理能力！
type: docs
weight: 5420
url: /zh/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

表示解析 JSON 数据的选项。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class JsonDataLoadOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | 使用默认选项初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | 获取或设置一个标志，指示生成的数据源是否始终包含 JSON 根元素的对象。如果 JSON 根元素包含单个复杂属性，则默认情况下不会创建此类对象。 |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | 获取或设置在加载 JSON 时解析 JSON 日期时间值的精确格式。默认值为`无效的`. |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | 获取或设置一个标志，指示在加载 JSON 数据的字符串值时是否应保留前导和尾随空格。 |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | 获取或设置在加载 JSON 时解析 JSON 简单值（null、boolean、number、integer 和 string）的模式。此模式不会影响日期时间值的解析。默认值为 Loose. |

## 评论

此类的实例可以传递到[`JsonDataSource`](../jsondatasource/).

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
