---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words for .NET
description: 了解 SplitOptions SplitCriteria 属性如何通过有效地将内容划分为可管理的部分来增强文档管理。
type: docs
weight: 20
url: /zh/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

指定将文档拆分为部分的标准。

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## 例子

显示如何按页面拆分文档。

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### 也可以看看

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
