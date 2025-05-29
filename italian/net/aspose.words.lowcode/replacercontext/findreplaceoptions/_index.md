---
title: ReplacerContext.FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words per .NET
description: Scopri la proprietà FindReplaceOptions di ReplacerContext per migliorare la funzionalità di ricerca e sostituzione con opzioni personalizzabili per risultati migliori.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/replacercontext/findreplaceoptions/
---
## ReplacerContext.FindReplaceOptions property

Opzioni di ricerca/sostituzione.

```csharp
public FindReplaceOptions FindReplaceOptions { get; }
```

## Esempi

Mostra come sostituire una stringa con un'espressione regolare nel documento utilizzando il contesto.

```csharp
// Esistono diversi modi per sostituire una stringa con un'espressione regolare nel documento:
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

Mostra come sostituire una stringa nel documento utilizzando il contesto.

```csharp
// Esistono diversi modi per sostituire una stringa nel documento:
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

Mostra come sostituire una stringa nel documento utilizzando i documenti dal flusso utilizzando il contesto.

```csharp
// Esistono diversi modi per sostituire una stringa nel documento utilizzando i documenti dal flusso:
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

Mostra come sostituire una stringa con un'espressione regolare nel documento utilizzando i documenti dal flusso utilizzando il contesto.

```csharp
// Esistono diversi modi per sostituire una stringa con un'espressione regolare nel documento utilizzando i documenti dal flusso:
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

### Guarda anche

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [ReplacerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
