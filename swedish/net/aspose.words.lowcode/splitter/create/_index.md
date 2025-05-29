---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words för .NET
description: Upptäck hur du effektivt skapar en ny instans av splitterprocessorn med vår lättförståeliga guide för sömlös integration och förbättrad prestanda.
type: docs
weight: 10
url: /sv/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Skapar en ny instans av splitterprocessorn.

```csharp
public static Splitter Create(SplitterContext context)
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

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
