---
title: NodeImporter
second_title: Aspose.Words per .NET API Reference
description: Consente di eseguire in modo efficiente limportazione ripetuta di nodi da un documento allaltro.
type: docs
weight: 3970
url: /it/net/aspose.words/nodeimporter/
---
## NodeImporter class

Consente di eseguire in modo efficiente l'importazione ripetuta di nodi da un documento all'altro.

```csharp
public class NodeImporter
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [NodeImporter](nodeimporter#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Inizializza una nuova istanza di[`NodeImporter`](../nodeimporter) classe. |
| [NodeImporter](nodeimporter#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Inizializza una nuova istanza di[`NodeImporter`](../nodeimporter) classe. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode)(Node, bool) | Importa un nodo da un documento a un altro. |

### Osservazioni

Aspose.Words fornisce funzionalità per copiare e spostare facilmente frammenti tra documenti Microsoft Word. Questo è noto come "importazione di nodi". Prima di poter inserire un frammento da un documento in un altro, è necessario "importarlo". L'importazione crea un clone profondo del nodo originale, pronto per essere inserito nel documento di destinazione .

Il modo più semplice per importare un nodo è utilizzare il file[`ImportNode`](../documentbase/importnode) metodo fornito dal[`DocumentBase`](../documentbase) oggetto.

Tuttavia, quando devi importare nodi da un documento all'altro più volte, è meglio usare il[`NodeImporter`](../nodeimporter) classe. Il[`NodeImporter`](../nodeimporter) La classe consente di ridurre al minimo il numero di stili ed elenchi creati nel documento di destinazione.

La copia o lo spostamento di frammenti da un documento di Microsoft Word a un altro presenta un numero di sfide tecniche per Aspose.Words. In un documento Word, gli stili e la formattazione dell'elenco sono archiviati centralmente, separatamente dal testo del documento. I paragrafi e le sequenze di testo fanno semplicemente riferimento agli stili tramite identificatori univoci interni.

Le sfide derivano dal fatto che stili ed elenchi sono diversi in documenti diversi. Ad esempio, per copiare un paragrafo formattato con lo stile Intestazione 1 da un documento all'altro, è necessario tenere conto di una serie di cose: decidere se copia lo stile Intestazione 1 da il documento di origine al documento di destinazione, clona il paragrafo, aggiorna il paragrafo clonato in modo che faccia riferimento allo stile Intestazione 1 corretto nel documento di destinazione. Se lo stile doveva essere copiato, tutti gli stili che esso i riferimenti (basati su style e sullo stile del paragrafo successivo) dovrebbero essere analizzati ed eventualmente copiati e così via. Esistono problemi simili quando si copiano paragrafi puntati o numerati perché Microsoft Word memorizza le definizioni degli elenchi separatamente dal testo.

Il[`NodeImporter`](../nodeimporter)class è come un contesto, che contiene le "tabelle di traduzione" durante l'importazione. Traduce correttamente tra stili ed elenchi nei documenti di origine e di destinazione.

### Esempi

Mostra come inserire il contenuto di un documento in un segnalibro in un altro documento.

```csharp
[Test]
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

        // Passa attraverso tutti i nodi a livello di blocco nel corpo della sezione,
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

* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
