---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words 的 XlsxDateTimeParsingMode 枚举，实现高效的文档文本解析。轻松识别文件中的日期和时间值！
type: docs
weight: 6510
url: /zh/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

指定如何解析文档文本以识别日期和时间值。

```csharp
public enum XlsxDateTimeParsingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| UseCurrentLocale | `0` | 当前线程设置的日期时间格式将优先用于解析字符串值。如果解析失败，则尝试其他常见的日期时间格式。 |
| Auto | `1` | 文档中使用的日期时间格式是自动确定的。这可能需要额外的时间。 |

## 例子

展示如何指定日期时间格式的自动检测。

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// 使用日期时间格式自动检测进行指定。
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
