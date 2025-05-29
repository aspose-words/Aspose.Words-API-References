---
title: Replacer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Methode „Replacer Create“ eine neue Instanz des effizienten Replacer-Prozessors für eine nahtlose Datentransformation generiert.
type: docs
weight: 10
url: /de/net/aspose.words.lowcode/replacer/create/
---
## Replacer.Create method

Erstellt eine neue Instanz des Ersetzungsprozessors.

```csharp
public static Replacer Create(ReplacerContext context)
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

* class [ReplacerContext](../../replacercontext/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
