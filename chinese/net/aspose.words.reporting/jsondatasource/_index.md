---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.Reporting.JsonDataSource 解锁强大的报表功能。轻松访问 JSON 数据，无缝集成到您的报表中。
type: docs
weight: 5430
url: /zh/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

提供对报告中使用的 JSON 文件或流的数据的访问。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class JsonDataSource
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | 使用解析 JSON 数据的默认选项，创建一个包含 JSON 流数据的新数据源。 |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | 使用解析 JSON 数据的默认选项，使用来自 JSON 文件的数据创建新的数据源。 |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | 使用指定的选项解析 JSON 数据，创建一个包含 JSON 流数据的新数据源。 |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | 使用指定的选项解析 JSON 数据，创建一个包含 JSON 文件中数据的新数据源。 |

## 评论

要在生成报告时访问相应文件或流的数据，请将此类的实例作为 数据源传递给以下之一[`ReportingEngine`](../reportingengine/).BuildReport 重载.

在模板文档中，如果顶级 JSON 元素是数组，则`JsonDataSource`实例应该以与 相同的方式处理DataTable 实例。如果顶级 JSON 元素 是一个对象，则`JsonDataSource`实例应该以与 相同的方式处理DataRow 实例。有关更多信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

在模板文档中，您可以使用 JSON 元素的类型值。为了方便起见，引擎将 JSON 简单类型集合 替换为以下集合：

* Nullable
* Nullable
* Nullable
* Nullable
* String

引擎根据 JSON 表示自动识别额外类型的值。

要覆盖 JSON 数据加载的默认行为，请初始化并传递[`JsonDataLoadOptions`](../jsondataloadoptions/)实例 到此类的构造函数。

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
