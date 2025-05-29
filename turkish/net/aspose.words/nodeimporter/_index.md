---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: .NET için Aspose.Words
description: Aspose.Words.NodeImporter ile belge düğümlerini zahmetsizce aktarın. İş akışınızı kolaylaştırın ve belge yönetimi verimliliğini bugün artırın!
type: docs
weight: 4900
url: /tr/net/aspose.words/nodeimporter/
---
## NodeImporter class

Düğümlerin bir belgeden diğerine tekrar tekrar içe aktarılmasını verimli bir şekilde gerçekleştirmeye olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public class NodeImporter
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Yeni bir örneğini başlatır`NodeImporter` sınıf. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Yeni bir örneğini başlatır`NodeImporter` sınıf. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Bir düğümü bir belgeden diğerine aktarır. |

## Notlar

Aspose.Words, Microsoft Word belgeleri arasında fragments 'yi kolayca kopyalama ve taşıma işlevi sağlar. Buna "node'ları içe aktarma" denir. Bir parçayı bir belgeden diğerine eklemeden önce, onu "içe aktarmanız" gerekir. İçe aktarma, orijinal düğümün derin bir klonunu oluşturur ve hedef belgeye eklenmeye hazır hale getirir.

Bir düğümü içe aktarmanın en basit yolu,[`ImportNode`](../documentbase/importnode/) method tarafından sağlanan[`DocumentBase`](../documentbase/) nesne.

Ancak, düğümleri bir belgeden diğerine birden çok kez içe aktarmanız gerektiğinde, kullanmak daha iyidir`NodeImporter` sınıf.`NodeImporter` sınıfı hedef belgede oluşturulan stil ve liste sayısını en aza indirmeye olanak tanır.

Parçaları bir Microsoft Word belgesinden diğerine kopyalamak veya taşımak Aspose.Words için bir dizi teknik zorluk sunar. Bir Word belgesinde, stiller ve liste biçimlendirmesi belgenin metninden ayrı olarak merkezi olarak saklanır. paragraphs ve metin dizileri stilleri yalnızca dahili benzersiz tanımlayıcılarla referans alır.

Zorluklar, stillerin ve listelerin farklı belgelerde farklı olmasından kaynaklanır. Örneğin, Başlık 1 stiliyle biçimlendirilmiş bir paragrafı bir belgeden diğerine kopyalamak için, bir dizi şey dikkate alınmalıdır: Başlık 1 stilini kaynak belgeden hedef belgeye kopyalayıp kopyalamayacağınıza karar verin, paragrafı klonlayın, klonlanan paragrafı hedef belgede doğru Başlık 1 stiline başvuracak şekilde güncelleyin. Stilin kopyalanması gerekiyorsa, başvurduğu tüm stiller (style ve sonraki paragraf stiline göre) analiz edilmeli ve muhtemelen onlar da kopyalanmalıdır, vb. Madde işaretli veya numaralı paragrafları kopyalarken de benzer sorunlar yaşanır, çünkü Microsoft Word liste tanımlarını metinden ayrı olarak depolar.

The`NodeImporter`sınıf, içe aktarma sırasında "çeviri tablolarını" tutan bir bağlam gibidir. Kaynak ve hedef belgelerdeki stiller ve listeler arasında doğru bir şekilde çeviri yapar.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
