---
title: ReplacingArgs.MatchNode
linktitle: MatchNode
articleTitle: MatchNode
second_title: .NET için Aspose.Words
description: Eşleşmenizin başladığı düğüme kolayca erişmek için ReplacingArgs MatchNode özelliğini keşfedin, böylece kodlama verimliliğinizi ve doğruluğunuzu artırın.
type: docs
weight: 40
url: /tr/net/aspose.words.replacing/replacingargs/matchnode/
---
## ReplacingArgs.MatchNode property

Eşleşmenin başlangıcını içeren düğümü alır.

```csharp
public Node MatchNode { get; }
```

## Örnekler

Bir bulma ve değiştirme işleminde bir eşleşmenin yerine tüm belgenin içeriğinin nasıl ekleneceğini gösterir.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
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

        // Eşleşen metni içeren paragraftan sonra bir belge ekle.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Eşleşen metne sahip paragrafı kaldır.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Bir paragraf veya tablonun ardından başka bir belgenin tüm düğümlerini ekler.
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
                // Bir bölümdeki son boş paragraf ise düğümü atla.
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

### Ayrıca bakınız

* class [Node](../../../aspose.words/node/)
* class [ReplacingArgs](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
