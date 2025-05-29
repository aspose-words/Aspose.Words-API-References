---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words LowCode ReplacerContext-Klasse für nahtlose Such- und Ersetzungsvorgänge, die die Automatisierung und Effizienz Ihrer Dokumente verbessern.
type: docs
weight: 4350
url: /de/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

Kontext der Suchen/Ersetzen-Operation.

```csharp
public class ReplacerContext : ProcessorContext
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ReplacerContext](replacercontext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | Optionen zum Suchen/Ersetzen. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Vom Prozessor verwendete Schriftarteinstellungen. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Vom Prozessor verwendete Dokumentlayoutoptionen. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Vom Prozessor verwendeter Warn-Callback. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | Legt das Muster und den Ersatz fest, die von der Such-/Ersetzungsoperation verwendet werden. |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | Legt das Muster und den Ersatz fest, die von der Such-/Ersetzungsoperation verwendet werden. |

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

* class [ProcessorContext](../processorcontext/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
