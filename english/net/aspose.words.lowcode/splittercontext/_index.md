---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.LowCode.SplitterContext class for efficient document splitting, enhancing your workflow with seamless integration and powerful functionality.
type: docs
weight: 4450
url: /net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

Document splitter context.

```csharp
public class SplitterContext : ProcessorContext
```

## Constructors

| Name | Description |
| --- | --- |
| [SplitterContext](splittercontext/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Font settings used by the processor. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Document layout options used by the processor. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | Document split options. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Warning callback used by the processor. |

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

* class [ProcessorContext](../processorcontext/)
* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
