---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words for .NET
description: 发现 XlsxSaveOptions 的 DateTimeParsingMode 属性来自定义文档如何解析日期和时间，确保准确的数据解释。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

获取或设置指定如何解析文档文本以识别日期和时间值的模式。 默认值为UseCurrentLocale.

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

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

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
