---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Reporting.ReportBuildOptions 枚举. 指定控制行为的选项ReportingEngine在构建报告时 在 C#.
type: docs
weight: 4720
url: /zh/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

指定控制行为的选项[`ReportingEngine`](../reportingengine/)在构建报告时。

```csharp
[Flags]
public enum ReportBuildOptions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 指定默认选项。 |
| AllowMissingMembers | `1` | 指定缺少的对象成员应被引擎视为空文字。此选项 仅影响对实例（即非静态）对象成员和扩展方法的访问。如果未设置此 选项，引擎在遇到缺少的对象成员时会抛出异常。 |
| RemoveEmptyParagraphs | `2` | 指定引擎应该在模板语法标记被 删除或替换为空值后删除变为空的段落。 |
| InlineErrorMessages | `4` | 指定引擎应将模板语法错误消息内联到输出文档中。 如果不设置此选项，引擎在遇到语法错误时会抛出异常。 |
| UseLegacyHeaderFooterVisiting | `8` | 指定引擎应该以与 Aspose.Words 21.9 之前的版本兼容的 order 访问节子节点（页眉、页脚、正文）。 |
| RespectJpegExifOrientation | `10` | 指定引擎应该使用EXIF图像方向值来适当地旋转inserted JPEG图像。 |

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
