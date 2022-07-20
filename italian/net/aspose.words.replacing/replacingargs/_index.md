---
title: ReplacingArgs
second_title: Aspose.Words per .NET API Reference
description: Fornisce i dati per unoperazione di sostituzione personalizzata.
type: docs
weight: 4390
url: /it/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Fornisce i dati per un'operazione di sostituzione personalizzata.

```csharp
public class ReplacingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex) { get; set; } | Identifica, per indice, un gruppo acquisito nel file[`Match`](./match) che deve essere sostituito con il[`Replacement`](./replacement) stringa. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname) { get; set; } | Identifica, per nome, un gruppo acquisito nel file[`Match`](./match) che deve essere sostituito con il[`Replacement`](./replacement) stringa. |
| [Match](../../aspose.words.replacing/replacingargs/match) { get; } | IlMatch risultante da una singola corrispondenza di espressioni regolari durante a **Sostituire** . |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode) { get; } | Ottiene il nodo che contiene l'inizio della corrispondenza. |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset) { get; } | Ottiene la posizione iniziale in base zero della corrispondenza dall'inizio di il nodo che contiene l'inizio della corrispondenza. |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement) { get; set; } | Ottiene o imposta la stringa di sostituzione. |

### Esempi

Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con un'altra stringa, tenendo traccia di tutte queste sostituzioni.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();

    // Imposta un callback che tenga traccia di tutte le sostituzioni che il metodo "Replace" effettuerà.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Mantiene un registro di ogni sostituzione di testo eseguita da un'operazione di ricerca e sostituzione
/// e annota il valore del testo corrispondente originale.
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

Mostra come inserire il contenuto di un intero documento in sostituzione di una corrispondenza in un'operazione di ricerca e sostituzione.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Inserisce un documento dopo il paragrafo contenente il testo corrispondente.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Rimuovi il paragrafo con il testo corrispondente.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Inserisce tutti i nodi di un altro documento dopo un paragrafo o una tabella.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Salta il nodo se è l'ultimo paragrafo vuoto in una sezione.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### Guarda anche

* interface [IReplacingCallback](../ireplacingcallback)
* class [Range](../../aspose.words/range)
* method [Replace](../../aspose.words/range/replace)
* spazio dei nomi [Aspose.Words.Replacing](../../aspose.words.replacing)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
