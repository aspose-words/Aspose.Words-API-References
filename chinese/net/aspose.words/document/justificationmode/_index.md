---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words for .NET
description: 了解如何使用 JustificationMode 属性优化文档的字符间距。轻松提升可读性并改善呈现效果！
type: docs
weight: 240
url: /zh/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

获取或设置文档的字符间距调整。

```csharp
public JustificationMode JustificationMode { get; set; }
```

## 例子

展示如何管理字符间距控制。

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### 也可以看看

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
