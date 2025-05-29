---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words för .NET
description: Upptäck hur du optimerar dokumenthanteringen med SplitterContexts SplitOptions-egenskap för effektiv och flexibel innehållsdelning. Förbättra ditt arbetsflöde idag.
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Alternativ för dokumentdelning.

```csharp
public SplitOptions SplitOptions { get; }
```

## Exempel

Visar hur man delar upp ett dokument efter sidor med hjälp av kontext.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Visar hur man delar upp ett dokument från strömmen efter sidor med hjälp av kontext.

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

### Se även

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
