---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words per .NET
description: Trasferisci facilmente i nodi tra i documenti con il metodo ImportNode di NodeImporter. Migliora il tuo flusso di lavoro e semplifica l'integrazione dei dati oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Importa un nodo da un documento a un altro.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | Node | Il nodo da importare. |
| isImportChildren | Boolean | `VERO` per importare tutti i nodi figlio in modo ricorsivo; altrimenti,`falso`. |

### Valore di ritorno

Il nodo clonato e importato. Il nodo appartiene al documento di destinazione, ma non ha un nodo padre.

## Osservazioni

L'importazione di un nodo crea una copia del nodo sorgente appartenente al documento importato. Il nodo restituito non ha un nodo padre. Il nodo sorgente non viene modificato o rimosso dal documento originale.

Prima che un nodo da un altro documento possa essere inserito in questo documento, è necessario importarlo. Durante l'importazione, le proprietà specifiche del documento, come i riferimenti a stili ed elenchi, vengono tradotte dal documento originale al documento importato. Dopo l'importazione, il nodo può essere inserito nella posizione appropriata nel documento utilizzando[`InsertBefore`](../../compositenode/insertbefore/) o [`InsertAfter`](../../compositenode/insertafter/).

Se il nodo sorgente appartiene già al documento di destinazione, viene semplicemente creato un clone profondo del nodo sorgente.

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

* class [Node](../../node/)
* class [NodeImporter](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
