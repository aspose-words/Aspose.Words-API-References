---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: 用于 .NET 的 Aspose.Words
description: Document JustificationMode 财产. 获取或设置文档的字符间距调整 在 C#.
type: docs
weight: 230
url: /zh/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

获取或设置文档的字符间距调整。

```csharp
public JustificationMode JustificationMode { get; set; }
```

## 例子

演示如何管理字符间距控制。

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
