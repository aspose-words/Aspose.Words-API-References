---
title: ReplacerContext.SetReplacement
linktitle: SetReplacement
articleTitle: SetReplacement
second_title: Aspose.Words per .NET
description: Ottimizza le operazioni di ricerca e sostituzione con il metodo SetReplacement di ReplacerContext, che consente una gestione fluida di modelli e sostituzioni per un'efficienza ottimale.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/replacercontext/setreplacement/
---
## SetReplacement(*string, string*) {#setreplacement}

Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione.

```csharp
public void SetReplacement(string pattern, string replacement)
```

## Osservazioni

L'utilizzo di questo metodo sovrascrive il modello e la sostituzione impostati in precedenza.

## Esempi

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

### Guarda anche

* class [ReplacerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetReplacement(*Regex, string*) {#setreplacement_1}

Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione.

```csharp
public void SetReplacement(Regex pattern, string replacement)
```

## Osservazioni

L'utilizzo di questo metodo sovrascrive il modello e la sostituzione impostati in precedenza.

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

* class [ReplacerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
