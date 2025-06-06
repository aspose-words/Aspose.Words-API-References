---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Underline 枚举，获取丰富的字体下划线选项。立即使用可自定义的样式增强您的文档格式！
type: docs
weight: 7360
url: /zh/net/aspose.words/underline/
---
## Underline enumeration

表示应用于字体的下划线类型。

```csharp
public enum Underline
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

## 例子

显示如何插入超链接字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// 插入超链接并使用自定义格式强调它。
// 超链接将是一段可点击的文本，它将带我们到 URL 中指定的位置。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// 按住 Ctrl 键并左键单击 Microsoft Word 中文本中的链接将通过新的 Web 浏览器窗口带我们进入 URL。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
