---
title: Paragraph.IsEndOfSection
linktitle: IsEndOfSection
articleTitle: IsEndOfSection
second_title: .NET için Aspose.Words
description: Paragraph IsEndOfSection özelliğini keşfedin, gelişmiş belge yapısı ve netlik için bir paragrafın bir bölümün ana metnindeki son paragraf olup olmadığını belirleyin.
type: docs
weight: 80
url: /tr/net/aspose.words/paragraph/isendofsection/
---
## Paragraph.IsEndOfSection property

Bu paragraf, paragrafın son paragrafıysa doğrudur.[`Body`](../../body/) (ana metin hikayesi)[`Section`](../../section/) ; aksi takdirde yanlış.

```csharp
public bool IsEndOfSection { get; }
```

## Örnekler

Bir belgenin içeriğinin başka bir belgedeki yer imine nasıl ekleneceğini gösterir.

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
/// Belirtilen düğümden sonra belgenin içeriğini ekler.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Bölümün gövdesindeki tüm blok düzeyindeki düğümler arasında döngü kur,
        // daha sonra bölümün son boş paragrafı olmayan her düğümü klonla ve ekle.
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

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
