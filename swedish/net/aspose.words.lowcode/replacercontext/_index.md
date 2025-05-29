---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words LowCode ReplacerContext-klassen för sömlösa sök- och ersättningsåtgärder, vilket förbättrar din dokumentautomation och effektivitet.
type: docs
weight: 4350
url: /sv/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

Hitta/ersätt operationskontext.

```csharp
public class ReplacerContext : ProcessorContext
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ReplacerContext](replacercontext/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | Hitta/ersätt alternativ. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Typsnittsinställningar som används av processorn. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Dokumentlayoutalternativ som används av processorn. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Varningsåteranrop som används av processorn. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | Ställer in mönster och ersättning som används av sök/ersätt-operationen. |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | Ställer in mönster och ersättning som används av sök/ersätt-operationen. |

## Exempel

Visar hur man ersätter sträng med regex i dokumentet med hjälp av kontext.

```csharp
// Det finns flera sätt att ersätta strängar med regex i dokumentet:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContextRegex.docx")
    .Execute();
```

Visar hur man ersätter strängar i dokumentet med hjälp av kontext.

```csharp
// Det finns flera sätt att ersätta strängar i dokumentet:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContext.docx")
    .Execute();
```

Visar hur man ersätter strängar i dokumentet med hjälp av dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att ersätta strängar i dokumentet med hjälp av dokument från strömmen:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

Visar hur man ersätter strängar med regex i dokumentet med hjälp av dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att ersätta strängar med regex i dokumentet med hjälp av dokument från strömmen:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStreamRegex.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Se även

* class [ProcessorContext](../processorcontext/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
