---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words per .NET
description: Trasferisci senza sforzo i nodi dei documenti con Aspose.Words.NodeImporter. Semplifica il tuo flusso di lavoro e migliora l'efficienza della gestione dei documenti oggi stesso!
type: docs
weight: 4900
url: /it/net/aspose.words/nodeimporter/
---
## NodeImporter class

Consente di eseguire in modo efficiente l'importazione ripetuta di nodi da un documento all'altro.

Per saperne di più, visita il[Modello a oggetti del documento (DOM) di Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class NodeImporter
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Inizializza una nuova istanza di`NodeImporter` classe. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Inizializza una nuova istanza di`NodeImporter` classe. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Importa un nodo da un documento a un altro. |

## Osservazioni

Aspose.Words offre funzionalità per copiare e spostare facilmente frammenti tra documenti di Microsoft Word. Questa operazione è nota come "importazione di nodi". Prima di poter inserire un frammento da un documento a un altro, è necessario "importarlo". L'importazione crea un clone completo del nodo originale, pronto per essere inserito nel documento di destinazione.

Il modo più semplice per importare un nodo è utilizzare[`ImportNode`](../documentbase/importnode/) metodo fornito da[`DocumentBase`](../documentbase/) oggetto.

Tuttavia, quando è necessario importare nodi da un documento all'altro più volte, è meglio utilizzare`NodeImporter` classe. La`NodeImporter` La classe consente di ridurre al minimo il numero di stili ed elenchi creati nel documento di destinazione.

Copiare o spostare frammenti da un documento Microsoft Word a un altro presenta una serie di sfide tecniche per Aspose.Words. In un documento Word, gli stili e la formattazione degli elenchi sono archiviati centralmente, separatamente dal testo del documento. I paragrafi e le sequenze di testo fanno semplicemente riferimento agli stili tramite identificatori univoci interni.

Le sfide nascono dal fatto che stili ed elenchi sono diversi in documenti diversi. Ad esempio, per copiare un paragrafo formattato con lo stile Titolo 1 da un documento a un altro, è necessario prendere in considerazione una serie di cose: decidere se copiare lo stile Titolo 1 dal documento di origine al documento di destinazione, clonare il paragrafo, aggiornare il paragrafo clonato in modo che faccia riferimento allo stile Titolo 1 corretto nel documento di destinazione. Se lo stile dovesse essere copiato, tutti gli stili a cui fa riferimento (in base allo stile e allo stile del paragrafo successivo) dovrebbero essere analizzati ed eventualmente copiati anch'essi e così via. Problemi simili si verificano quando si copiano paragrafi puntati o numerati perché Microsoft Word memorizza le definizioni degli elenchi separatamente dal testo.

IL`NodeImporter`La classe è come un contesto, che contiene le "tabelle di traduzione" durante l'importazione. Traduce correttamente tra stili ed elenchi nei documenti di origine e di destinazione.

## Esempi

Mostra come inserire il contenuto di un documento in un segnalibro di un altro documento.

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// Inserisce il contenuto di un documento dopo il nodo specificato.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Esegue un ciclo attraverso tutti i nodi a livello di blocco nel corpo della sezione,
        // quindi clona e inserisci ogni nodo che non sia l'ultimo paragrafo vuoto di una sezione.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
