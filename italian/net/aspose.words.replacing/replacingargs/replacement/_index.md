---
title: ReplacingArgs.Replacement
linktitle: Replacement
articleTitle: Replacement
second_title: Aspose.Words per .NET
description: Scopri la proprietà Replacement ReplacingArgs per gestire e personalizzare facilmente le stringhe di sostituzione per una maggiore efficienza di codifica.
type: docs
weight: 60
url: /it/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

Ottiene o imposta la stringa sostitutiva.

```csharp
public string Replacement { get; set; }
```

## Esempi

Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con un'altra stringa, tenendo traccia di tutte le sostituzioni.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Imposta un callback che tiene traccia di tutte le sostituzioni effettuate dal metodo "Replace".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Mantiene un registro di ogni sostituzione di testo effettuata tramite un'operazione di ricerca e sostituzione
/// e annota il valore del testo originale corrispondente.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Guarda anche

* class [ReplacingArgs](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
