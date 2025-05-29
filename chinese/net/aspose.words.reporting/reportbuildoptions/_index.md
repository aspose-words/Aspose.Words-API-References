---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words ReportingEngine 选项，高效创建报表。灵活设置，自定义报表，获得最佳效果。
type: docs
weight: 5460
url: /zh/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

指定控制行为的选项[`ReportingEngine`](../reportingengine/)正在构建报告。

```csharp
[Flags]
public enum ReportBuildOptions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 指定默认选项。 |
| AllowMissingMembers | `1` | 指定引擎应将缺失的对象成员视为空值。此选项 仅影响对实例（即非静态）对象成员和扩展方法的访问。如果未设置此 选项，则引擎在遇到缺失的对象成员时会抛出异常。 |
| RemoveEmptyParagraphs | `2` | 指定引擎应在模板语法标签被删除或替换为空值后删除变为空的段落。 |
| InlineErrorMessages | `4` | 指定引擎应将模板语法错误消息内联到输出文档中。 如果未设置此选项，则引擎在遇到语法错误时会引发异常。 |
| UseLegacyHeaderFooterVisiting | `8` | 指定引擎应按顺序访问部分子节点（页眉、页脚、正文），与 21.9 之前的 Aspose.Words 版本兼容。 |
| RespectJpegExifOrientation | `10` | 指定引擎应使用 EXIF 图像方向值来适当旋转插入的 JPEG 图像。 |
| UpdateFieldsSyntaxAware | `20` | 指定引擎应忽略字段结果中的模板语法并在报告构建后更新字段。 |

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
