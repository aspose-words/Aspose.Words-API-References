---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words for .NET
description: Aspose.Words.NodeImporter sınıf. Düğümlerin bir belgeden diğerine tekrar tekrar içe aktarılmasının verimli bir şekilde gerçekleştirilmesine olanak tanır C#'da.
type: docs
weight: 4210
url: /tr/net/aspose.words/nodeimporter/
---
## NodeImporter class

Düğümlerin bir belgeden diğerine tekrar tekrar içe aktarılmasının verimli bir şekilde gerçekleştirilmesine olanak tanır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

```csharp
public class NodeImporter
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Yeni bir örneğini başlatır`NodeImporter` class. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Yeni bir örneğini başlatır`NodeImporter` class. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Bir belgedeki düğümü diğerine aktarır. |

## Notlar

Aspose.Words, fragments 'nin Microsoft Word belgeleri arasında kolayca kopyalanması ve taşınması için işlevsellik sağlar. Bu, "düğümlerin içe aktarılması" olarak bilinir. Bir belgeden diğerine bir parça ekleyebilmeniz için önce onu "içe aktarmanız" gerekir. İçe aktarma, orijinal düğümün, hedef belgesine eklenmeye hazır derin bir klonunu oluşturur.

Bir düğümü içe aktarmanın en basit yolu,[`ImportNode`](../documentbase/importnode/) method tarafından sağlanmıştır[`DocumentBase`](../documentbase/) nesne.

Ancak, düğümleri bir belgeden diğerine birden çok kez aktarmanız gerektiğinde, öğesini kullanmak daha iyidir`NodeImporter` sınıf.`NodeImporter` sınıfı, hedef belgede oluşturulan stil ve listelerin sayısını en aza indirmeye olanak tanır.

Parçaları bir Microsoft Word belgesinden diğerine kopyalamak veya taşımak, Aspose.Words için x000d_ sayıda teknik zorluk teşkil eder. Bir Word belgesinde stiller ve liste biçimlendirme , belgenin metninden ayrı olarak merkezi olarak depolanır. Paragraflar ve metin dizileri yalnızca dahili benzersiz tanımlayıcılarla stillere atıfta bulunur.

Zorluklar, stillerin ve listelerin farklı belgelerde farklı olmasından kaynaklanmaktadır. Örneğin, Başlık 1 stiliyle biçimlendirilmiş bir paragrafı bir belgeden diğerine kopyalamak için bir dizi şeyin dikkate alınması gerekir: bunun yapılıp yapılmayacağına karar verin Başlık 1 stilini kaynak belgeden hedef belgeye kopyalayın, paragrafı kopyalayın, cloned paragrafını hedef belgedeki doğru Başlık 1 stiline atıfta bulunacak şekilde güncelleyin. Stilin kopyalanması gerekiyorsa, kopyalandığı tüm stiller referanslar (style ve sonraki paragraf stiline dayalı olarak) analiz edilmeli ve muhtemelen kopyalanmalıdır, vb.. Microsoft Word , liste tanımlarını metinden ayrı olarak sakladığından, madde işaretli veya numaralı paragrafları kopyalarken benzer sorunlar ortaya çıkar.

`NodeImporter`sınıf, içe aktarma sırasında "çeviri tablolarını" tutan bir bağlam gibidir. Kaynak ve hedef belgelerdeki stiller ve listeler arasında doğru şekilde çeviri yapar.

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
/// Belgenin içeriğini belirtilen düğümden sonra ekler.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Bölümün gövdesindeki tüm blok düzeyindeki düğümler arasında döngü yapın,
        // sonra bir bölümün son boş paragrafı olmayan her düğümü kopyalayıp ekleyin.
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
