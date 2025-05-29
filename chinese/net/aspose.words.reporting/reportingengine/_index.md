---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.ReportingEngine 解锁强大的文档自动化功能。轻松将数据填充到模板中，并自定义设置，实现无缝报表生成。
type: docs
weight: 5470
url: /zh/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

提供例程以使用数据填充模板文档和一组设置来控制这些例程。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class ReportingEngine
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ReportingEngine](reportingengine/)() | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | 获取包含以下项的无序集合（即唯一项的集合）Type对象 的完全或部分限定名称可在由此引擎 实例处理的报告模板中使用，以调用相应类型的静态成员、执行类型转换等。 |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | 获取或设置打印的字符串值，而不是模板表达式，该值表示对对象缺失成员的简单引用。默认值为空字符串。 |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | 获取或设置一组控制此行为的标志`ReportingEngine`实例 ，同时构建报告。 |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | 获取或设置一个值，指示通过反射 API 执行的自定义类型成员调用是否使用动态类生成进行优化。默认值为`真的`. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | 使用来自指定源的数据填充指定的模板文档，使其成为一份现成的报告。 |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | 使用来自指定源的数据填充指定的模板文档，使其成为一份现成的报告。 |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | 使用来自指定来源的数据填充指定的模板文档，使其成为一份现成的报告。 |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | 返回类型，哪些成员以及哪些派生类型的成员应该不能被引擎通过模板语法访问。 |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | 指定类型，哪些成员以及哪些派生类型的成员应该不能被引擎通过模板语法访问。 |

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
