---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: 通过我们易于遵循的指南，了解如何有效地创建分离器处理器的新实例，以实现无缝集成和增强性能。
type: docs
weight: 10
url: /zh/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

创建分离器处理器的新实例。

```csharp
public static Splitter Create(SplitterContext context)
```

## 例子

展示如何使用上下文按页面拆分文档。

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

展示如何使用上下文按页面从流中拆分文档。

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### 也可以看看

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
