---
title: NodeImporter.NodeImporter
second_title: Aspose.Words per .NET API Reference
description: NodeImporter costruttore. Inizializza una nuova istanza diNodeImporter classe.
type: docs
weight: 10
url: /it/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

Inizializza una nuova istanza di[`NodeImporter`](../) classe.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | DocumentBase | Il documento di origine. |
| dstDoc | DocumentBase | Il documento di destinazione che sarà il proprietario dei nodi importati. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione dello stile in conflitto. |

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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* spazio dei nomi [Aspose.Words](../../nodeimporter/)
* assemblea [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

Inizializza una nuova istanza di[`NodeImporter`](../) classe.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | DocumentBase | Il documento di origine. |
| dstDoc | DocumentBase | Il documento di destinazione che sarà il proprietario dei nodi importati. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione dello stile in conflitto. |
| importFormatOptions | ImportFormatOptions | Specifica varie opzioni per formattare il nodo importato. |

### Esempi

Mostra come risolvere un conflitto durante l'importazione di documenti che hanno elenchi con lo stesso identificatore di definizione elenco.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Imposta la proprietà "KeepSourceNumbering" su "true" per applicare un ID di definizione elenco diverso
// in stili identici a quelli di Aspose.Words li importa nei documenti di destinazione.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Mostra come risolvere i conflitti di numerazione degli elenchi nei documenti di origine e di destinazione.

```csharp
// Apre un documento con uno schema di numerazione elenco personalizzato, quindi clonalo.
// Poiché entrambi hanno lo stesso formato di numerazione, i formati si scontreranno se importiamo un documento nell'altro.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Quando importiamo il clone del documento nell'originale e poi lo aggiungiamo,
// quindi si uniranno i due elenchi con lo stesso formato di elenco.
// Se impostiamo il flag "KeepSourceNumbering" su "false", l'elenco dal documento clone
// che aggiungiamo all'originale continuerà la numerazione dell'elenco a cui lo aggiungiamo.
// Questo unirà efficacemente le due liste in una sola.
// Se impostiamo il flag "KeepSourceNumbering" su "true", il documento clona
// list manterrà la sua numerazione originale, facendo apparire le due liste come liste separate. 
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Guarda anche

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* spazio dei nomi [Aspose.Words](../../nodeimporter/)
* assemblea [Aspose.Words](../../../)


