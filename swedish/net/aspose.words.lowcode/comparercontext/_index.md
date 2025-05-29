---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words LowCode ComparerContext-klassen för effektiv dokumentjämförelse, förbättra ditt arbetsflöde med sömlös integration och kraftfulla funktioner.
type: docs
weight: 4220
url: /sv/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Dokumentjämförare context

```csharp
public class ComparerContext : ProcessorContext
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ComparerContext](comparercontext/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Anger om revisioner i dokumenten ska accepteras innan de jämförs. Om de jämförda dokumenten innehåller revisioner och denna flagga är inställd på falskt, kommer processorn att avvisa revisioner. Standard är`sann` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | Författaren som ska tilldelas revisioner som skapats under dokumentjämförelsen. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Alternativ som används vid jämförelse av dokument. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | Datum och tid som tilldelats revisioner som skapats under dokumentjämförelsen. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Typsnittsinställningar som används av processorn. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Dokumentlayoutalternativ som används av processorn. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Varningsåteranrop som används av processorn. |

## Exempel

Visar hur man enkelt jämför dokument med hjälp av kontext.

```csharp
// Det finns flera sätt att jämföra dokument:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

Visar hur man jämför dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att jämföra dokument från strömmen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### Se även

* class [ProcessorContext](../processorcontext/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
