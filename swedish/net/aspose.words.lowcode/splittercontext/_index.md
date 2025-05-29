---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.LowCode.SplitterContext för effektiv dokumentdelning, vilket förbättrar ditt arbetsflöde med sömlös integration och kraftfull funktionalitet.
type: docs
weight: 4430
url: /sv/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

Dokumentdelningskontext.

```csharp
public class SplitterContext : ProcessorContext
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [SplitterContext](splittercontext/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Typsnittsinställningar som används av processorn. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Dokumentlayoutalternativ som används av processorn. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | Alternativ för dokumentdelning. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Varningsåteranrop som används av processorn. |

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

* class [ProcessorContext](../processorcontext/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
