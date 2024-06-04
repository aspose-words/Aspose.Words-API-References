---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Reporting.ReportBuildOptions enum. Specifies options controlling behavior of ReportingEngine while building a report in C#.
type: docs
weight: 4950
url: /net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Specifies options controlling behavior of [`ReportingEngine`](../reportingengine/) while building a report.

```csharp
[Flags]
public enum ReportBuildOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Specifies default options. |
| AllowMissingMembers | `1` | Specifies that missing object members should be treated as null literals by the engine. This option affects only access to instance (that is, non-static) object members and extension methods. If this option is not set, the engine throws an exception when encounters a missing object member. |
| RemoveEmptyParagraphs | `2` | Specifies that the engine should remove paragraphs becoming empty after template syntax tags are removed or replaced with empty values. |
| InlineErrorMessages | `4` | Specifies that the engine should inline template syntax error messages into output documents. If this option is not set, the engine throws an exception when encounters a syntax error. |
| UseLegacyHeaderFooterVisiting | `8` | Specifies that the engine should visit section child nodes (headers, footers, bodies) in an order compatible with Aspose.Words versions prior 21.9. |
| RespectJpegExifOrientation | `10` | Specifies that the engine should use EXIF ​​image orientation values to appropriately rotate inserted JPEG images. |
| UpdateFieldsSyntaxAware | `20` | Specifies that the engine should ignore template syntax in field results and update fields after a report is built. |

### See Also

* namespace [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assembly [Aspose.Words](../../)
