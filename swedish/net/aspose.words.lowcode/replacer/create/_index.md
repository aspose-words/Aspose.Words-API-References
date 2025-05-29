---
title: Replacer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words för .NET
description: Upptäck hur metoden Replacer Create genererar en ny instans av den effektiva ersättningsprocessorn för sömlös datatransformation.
type: docs
weight: 10
url: /sv/net/aspose.words.lowcode/replacer/create/
---
## Replacer.Create method

Skapar en ny instans av ersättningsprocessorn.

```csharp
public static Replacer Create(ReplacerContext context)
```

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

* class [ReplacerContext](../../replacercontext/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
