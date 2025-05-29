---
title: ReplacingArgs Class
linktitle: ReplacingArgs
articleTitle: ReplacingArgs
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Replacing.ReplacingArgs per una sostituzione efficiente del testo personalizzato nei tuoi documenti. Migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 5390
url: /it/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Fornisce dati per un'operazione di sostituzione personalizzata.

Per saperne di più, visita il[Trova e sostituisci](https://docs.aspose.com/words/net/find-and-replace/) articolo di documentazione.

```csharp
public class ReplacingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex/) { get; set; } | Identifica, tramite indice, un gruppo catturato nel[`Match`](./match/) che deve essere sostituito con il[`Replacement`](./replacement/) stringa. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname/) { get; set; } | Identifica, per nome, un gruppo catturato nel[`Match`](./match/) che deve essere sostituito con il[`Replacement`](./replacement/) stringa. |
| [Match](../../aspose.words.replacing/replacingargs/match/) { get; } | IlMatch risultante da una singola corrispondenza di espressione regular durante un**Sostituire** . |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode/) { get; } | Ottiene il nodo che contiene l'inizio della corrispondenza. |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset/) { get; } | Ottiene la posizione iniziale a partire da zero della corrispondenza dall'inizio di il nodo che contiene l'inizio della corrispondenza. |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement/) { get; set; } | Ottiene o imposta la stringa sostitutiva. |

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

Mostra come inserire il contenuto di un intero documento in sostituzione di una corrispondenza in un'operazione di ricerca e sostituzione.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* spazio dei nomi [Aspose.Words.Replacing](../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../)
