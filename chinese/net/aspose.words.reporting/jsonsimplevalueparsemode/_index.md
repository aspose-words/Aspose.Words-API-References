---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Reporting.JsonSimpleValueParseMode 枚举. 指定加载 JSON 时解析 JSON 简单值空布尔值数字整数和字符串的模式 这种模式不会影响日期时间值的解析 在 C#.
type: docs
weight: 4700
url: /zh/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

指定加载 JSON 时解析 JSON 简单值（空、布尔值、数字、整数和字符串）的模式。 这种模式不会影响日期时间值的解析。

```csharp
public enum JsonSimpleValueParseMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Loose | `0` | 指定在解析字符串表示形式时确定 JSON 简单值的类型的模式。 例如，在此模式下，JSON 片段“{ prop: "123" }”中的“prop”类型被确定为整数。 |
| Strict | `1` | 指定根据 JSON 表示法本身确定 JSON 简单值类型的模式。 例如，在此模式下，JSON 片段 '{ prop: "123" }' 中的 'prop' 类型被确定为字符串。 |

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
