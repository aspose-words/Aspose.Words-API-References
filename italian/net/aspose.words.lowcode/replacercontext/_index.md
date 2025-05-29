---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words LowCode ReplacerContext per operazioni di ricerca e sostituzione fluide, migliorando l'automazione e l'efficienza dei tuoi documenti.
type: docs
weight: 4350
url: /it/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

Contesto dell'operazione Trova/Sostituisci.

```csharp
public class ReplacerContext : ProcessorContext
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ReplacerContext](replacercontext/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | Opzioni di ricerca/sostituzione. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Impostazioni del font utilizzate dal processore. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opzioni di layout del documento utilizzate dal processore. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Callback di avviso utilizzato dal processore. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione. |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione. |

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

* class [ProcessorContext](../processorcontext/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
