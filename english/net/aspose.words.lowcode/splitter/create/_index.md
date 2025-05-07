---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: Discover how to efficiently create a new instance of the splitter processor with our easy-to-follow guide for seamless integration and enhanced performance.
type: docs
weight: 10
url: /net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Creates new instance of the splitter processor.

```csharp
public static Splitter Create(SplitterContext context)
```

## Examples

Shows how to split document by pages using context.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Shows how to split document from the stream by pages using context.

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

### See Also

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
