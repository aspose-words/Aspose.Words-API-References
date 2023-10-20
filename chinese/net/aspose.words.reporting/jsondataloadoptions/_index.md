---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Reporting.JsonDataLoadOptions 班级. 表示解析 JSON 数据的选项 在 C#.
type: docs
weight: 4680
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
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | 获取或设置一个标志，该标志指示生成的数据源是否始终包含 JSON root 元素的对象。如果 JSON 根元素包含单个复杂属性，则默认情况下不会创建此类对象。 |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | 获取或设置加载 JSON 时解析 JSON 日期时间值的精确格式。默认为`无效的`. |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | 获取或设置一个标志，该标志指示在加载 JSON 数据的 string 值时是否应保留前导空格和尾随空格。 |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | 获取或设置加载 JSON 时解析 JSON 简单值（空、布尔值、数字、整数和字符串） 的模式。这种模式不会影响日期时间值的解析。默认为 Loose. |

## 评论

此类的实例可以传递到构造函数中[`JsonDataSource`](../jsondatasource/).

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
