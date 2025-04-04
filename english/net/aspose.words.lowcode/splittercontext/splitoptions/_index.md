---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words for .NET
description: Discover how to optimize document management with SplitterContext's SplitOptions property for efficient and flexible content splitting. Enhance your workflow today.
type: docs
weight: 20
url: /net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Document split options.

```csharp
public SplitOptions SplitOptions { get; }
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

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
