---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Saving.MarkdownOfficeMathExportMode 如何增强 OfficeMath 到 Markdown 的导出功能，确保文档转换准确高效。
type: docs
weight: 6050
url: /zh/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

指定 Aspose.Words 如何将 OfficeMath 导出到 Markdown。

```csharp
public enum MarkdownOfficeMathExportMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Text | `0` | 将 OfficeMath 导出为纯文本。 |
| Image | `1` | 将 OfficeMath 导出为图像。 |
| MathML | `2` | 将 OfficeMath 导出为 MathML。 |

## 例子

显示如何将 OfficeMath 写入文档。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
