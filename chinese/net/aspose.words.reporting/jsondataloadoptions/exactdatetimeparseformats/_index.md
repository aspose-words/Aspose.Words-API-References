---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: 用于 .NET 的 Aspose.Words
description: JsonDataLoadOptions ExactDateTimeParseFormats 财产. 获取或设置加载 JSON 时解析 JSON 日期时间值的精确格式默认为无效的 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

获取或设置加载 JSON 时解析 JSON 日期时间值的精确格式。默认为`无效的`.

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## 评论

使用 Microsoft® JSON 日期时间格式编码的字符串（例如“/Date(1224043200000)/”）始终被 识别为日期时间值，无论此属性的值如何。该属性定义了在按以下方式解析字符串中的日期时间值时要使用的附加 格式：

* 当`ExactDateTimeParseFormats`是`无效的`、ISO-8601 格式以及当前美国英语和新西兰英语文化支持的所有日期时间格式 均按上述顺序另外使用 。
* 当`ExactDateTimeParseFormats`包含字符串，它们被用作利用当前区域性的附加日期时间 格式。
* 当`ExactDateTimeParseFormats`为空，未使用其他日期时间格式。

### 也可以看看

* class [JsonDataLoadOptions](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
