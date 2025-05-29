---
title: Paragraph.IsEndOfSection
linktitle: IsEndOfSection
articleTitle: IsEndOfSection
second_title: Aspose.Words per .NET
description: Scopri la proprietà Paragraph IsEndOfSection, identifica se un paragrafo è l'ultimo nel testo principale di una sezione per migliorare la struttura e la chiarezza del documento.
type: docs
weight: 80
url: /it/net/aspose.words/paragraph/isendofsection/
---
## Paragraph.IsEndOfSection property

Vero se questo paragrafo è l'ultimo paragrafo nel[`Body`](../../body/) (testo principale della storia) di un[`Section`](../../section/) ; falso altrimenti.

```csharp
public bool IsEndOfSection { get; }
```

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

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
