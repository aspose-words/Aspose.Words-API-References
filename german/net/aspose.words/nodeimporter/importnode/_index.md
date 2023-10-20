---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words für .NET
description: NodeImporter ImportNode methode. Importiert einen Knoten aus einem Dokument in ein anderes in C#.
type: docs
weight: 20
url: /de/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

Importiert einen Knoten aus einem Dokument in ein anderes.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | Node | Der zu importierende Knoten. |
| isImportChildren | Boolean | `WAHR` um alle untergeordneten Knoten rekursiv zu importieren; ansonsten,`FALSCH`. |

### Rückgabewert

Der geklonte, importierte Knoten. Der Knoten gehört zum Zieldokument, hat aber keinen übergeordneten Knoten.

## Bemerkungen

Beim Importieren eines Knotens wird eine Kopie des Quellknotens erstellt, der zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen übergeordneten Knoten. Der Quellknoten wird nicht geändert oder aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss dieser importiert werden. Beim Import werden dokumentspezifische Eigenschaften wie Verweise auf Stile und Listen vom Original in das importierende Dokument übersetzt . Nachdem der Knoten importiert wurde, kann er mit an der entsprechenden Stelle im Dokument eingefügt werden[`InsertBefore`](../../compositenode/insertbefore/) oder [`InsertAfter`](../../compositenode/insertafter/).

Wenn der Quellknoten bereits zum Zieldokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

## Beispiele

Zeigt, wie der Inhalt eines Dokuments in ein Lesezeichen in einem anderen Dokument eingefügt wird.

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
/// Fügt den Inhalt eines Dokuments nach dem angegebenen Knoten ein.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Alle Knoten auf Blockebene im Hauptteil des Abschnitts durchlaufen,
        // dann jeden Knoten klonen und einfügen, der nicht der letzte leere Absatz eines Abschnitts ist.
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

### Siehe auch

* class [Node](../../node/)
* class [NodeImporter](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
