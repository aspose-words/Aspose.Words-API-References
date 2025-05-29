---
title: ReplacerContext.FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FindReplaceOptions de ReplacerContext pour améliorer votre fonctionnalité de recherche et de remplacement avec des options personnalisables pour de meilleurs résultats.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/replacercontext/findreplaceoptions/
---
## ReplacerContext.FindReplaceOptions property

Options de recherche/remplacement.

```csharp
public FindReplaceOptions FindReplaceOptions { get; }
```

## Exemples

Montre comment remplacer une chaîne par une expression régulière dans le document à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document :
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

Montre comment remplacer une chaîne dans le document à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document :
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

Montre comment remplacer une chaîne dans le document à l'aide de documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document à l'aide de documents du flux :
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

Montre comment remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux :
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

### Voir également

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [ReplacerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
