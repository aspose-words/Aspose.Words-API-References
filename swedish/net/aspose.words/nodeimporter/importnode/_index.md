---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words för .NET
description: Överför enkelt noder mellan dokument med NodeImporters ImportNode-metod. Förbättra ditt arbetsflöde och effektivisera dataintegrationen idag!
type: docs
weight: 20
url: /sv/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Importerar en nod från ett dokument till ett annat.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcNode | Node | Noden som ska importeras. |
| isImportChildren | Boolean | `sann` att importera alla underordnade noder rekursivt; annars,`falsk`. |

### Returvärde

Den klonade, importerade noden. Noden tillhör destinationsdokumentet, men har ingen överordnad nod.

## Anmärkningar

Import av en nod skapar en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras eller tas inte bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under importen översätts dokumentspecifika egenskaper, såsom referenser till format och listor, från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med hjälp av[`InsertBefore`](../../compositenode/insertbefore/) eller [`InsertAfter`](../../compositenode/insertafter/).

Om källnoden redan tillhör destinationsdokumentet skapas helt enkelt en djup clone av källnoden.

## Exempel

Visar hur man infogar innehållet i ett dokument till ett bokmärke i ett annat dokument.

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
/// Infogar innehållet i ett dokument efter den angivna noden.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Loopa igenom alla blocknivånoder i sektionens brödtext,
        // klona och infoga sedan varje nod som inte är det sista tomma stycket i ett avsnitt.
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

### Se även

* class [Node](../../node/)
* class [NodeImporter](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
