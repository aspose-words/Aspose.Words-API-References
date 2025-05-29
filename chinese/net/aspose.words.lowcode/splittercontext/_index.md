---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.LowCode.SplitterContext 类以实现高效的文档拆分，通过无缝集成和强大的功能增强您的工作流程。
type: docs
weight: 4430
url: /zh/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

文档分割器上下文。

```csharp
public class SplitterContext : ProcessorContext
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [SplitterContext](splittercontext/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | 处理器使用的字体设置。 |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | 处理器使用的文档布局选项。 |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | 文档拆分选项。 |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | 处理器使用的警告回调。 |

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

* class [ProcessorContext](../processorcontext/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
