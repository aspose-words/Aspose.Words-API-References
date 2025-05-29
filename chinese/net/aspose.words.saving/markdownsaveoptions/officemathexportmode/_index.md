---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words for .NET
description: 探索 MarkdownSaveOptions OfficeMathExportMode 属性，自定义 OfficeMath 输出。使用灵活的导出设置优化您的文件！
type: docs
weight: 120
url: /zh/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

指定 OfficeMath 如何写入输出文件。 默认值为Text.

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## 例子

显示如何将 OfficeMath 写入文档。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### 也可以看看

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
