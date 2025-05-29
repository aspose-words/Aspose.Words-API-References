---
title: ReplacerContext.FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die FindReplaceOptions-Eigenschaft von ReplacerContext, um Ihre Such- und Ersetzungsfunktion mit anpassbaren Optionen für bessere Ergebnisse zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/replacercontext/findreplaceoptions/
---
## ReplacerContext.FindReplaceOptions property

Optionen zum Suchen/Ersetzen.

```csharp
public FindReplaceOptions FindReplaceOptions { get; }
```

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument mithilfe des Kontexts durch reguläre Ausdrücke ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument durch reguläre Ausdrücke zu ersetzen:
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

Zeigt, wie Zeichenfolgen im Dokument mithilfe des Kontexts ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument zu ersetzen:
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

Zeigt, wie Zeichenfolgen im Dokument mithilfe von Dokumenten aus dem Stream unter Verwendung des Kontexts ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument durch Dokumente aus dem Stream zu ersetzen:
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

Zeigt, wie Zeichenfolgen im Dokument mithilfe von Dokumenten aus dem Stream unter Verwendung des Kontexts durch reguläre Ausdrücke ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument mithilfe von Dokumenten aus dem Stream durch reguläre Ausdrücke zu ersetzen:
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

### Siehe auch

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [ReplacerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
