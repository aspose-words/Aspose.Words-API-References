---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words per .NET
description: NodeImporter ImportNode metodo. Importa un nodo da un documento in un altro in C#.
type: docs
weight: 20
url: /it/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Importa un nodo da un documento in un altro.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | Node | Il nodo da importare. |
| isImportChildren | Boolean | `VERO` per importare ricorsivamente tutti i nodi figlio; Altrimenti,`falso`. |

### Valore di ritorno

Il nodo clonato e importato. Il nodo appartiene al documento di destinazione, ma non ha un genitore.

## Osservazioni

L'importazione di un nodo crea una copia del nodo di origine appartenente al documento di importazione. Il nodo restituito non ha genitore. Il nodo di origine non viene alterato o rimosso dal documento originale.

Prima che un nodo di un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento come i riferimenti a stili ed elenchi vengono tradotte dal documento originale al documento importato. Dopo che il nodo è stato importato, può essere inserito nella posizione appropriata nel documento utilizzando[`InsertBefore`](../../compositenode/insertbefore/) o [`InsertAfter`](../../compositenode/insertafter/).

Se il nodo di origine appartiene già al documento di destinazione, viene semplicemente creato un deep clone del nodo di origine.

## Esempi

Mostra come inserire il contenuto di un documento in un segnalibro in un altro documento.

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

        // Passa attraverso tutti i nodi a livello di blocco nel corpo della sezione,
        // quindi clona e inserisce ogni nodo che non sia l'ultimo paragrafo vuoto di una sezione.
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
