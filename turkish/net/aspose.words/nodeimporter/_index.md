---
title: NodeImporter
second_title: Aspose.Words for .NET API Referansı
description: Bir belgeden diğerine düğümlerin tekrar tekrar içe aktarılmasını verimli bir şekilde gerçekleştirmeyi sağlar.
type: docs
weight: 3970
url: /tr/net/aspose.words/nodeimporter/
---
## NodeImporter class

Bir belgeden diğerine düğümlerin tekrar tekrar içe aktarılmasını verimli bir şekilde gerçekleştirmeyi sağlar.

```csharp
public class NodeImporter
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Yeni bir örneğini başlatır[`NodeImporter`](./nodeimporter/) sınıf. |
| [NodeImporter](nodeimporter/#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Yeni bir örneğini başlatır[`NodeImporter`](./nodeimporter/) sınıf. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(Node, bool) | Bir düğümü bir belgeden diğerine aktarır. |

### Notlar

Aspose.Words, Microsoft Word belgeleri arasında parçaları kolay kopyalama ve taşıma için işlevsellik sağlar. Bu, "düğümleri içe aktarma" olarak bilinir. Bir belgeden diğerine bir parça eklemeden önce, onu "içe aktarmanız" gerekir. İçe aktarma, orijinal düğümün hedef belgesine eklenmeye hazır derin bir klonunu oluşturur.

Bir düğümü içe aktarmanın en basit yolu,[`ImportNode`](../documentbase/importnode/) tarafından sağlanan method [`DocumentBase`](../documentbase/) nesne.

Ancak, düğümleri bir belgeden diğerine birden çok kez aktarmanız gerektiğinde, [`NodeImporter`](./nodeimporter/) sınıf. bu[`NodeImporter`](./nodeimporter/) sınıfı, hedef belgede oluşturulan stil ve liste sayısını en aza indirmeye olanak tanır.

Parçaları bir Microsoft Word belgesinden diğerine kopyalamak veya taşımak, Aspose.Words için bir dizi teknik zorluk sunar. Bir Word belgesinde, stiller ve liste formatting , belgenin metninden ayrı olarak merkezi olarak depolanır. Paragrafs ve metin dizileri, yalnızca dahili benzersiz tanımlayıcılarla stillere başvurur.

Zorluklar, stillerin ve listelerin farklı belgelerde farklı olmasından kaynaklanmaktadır. Örneğin, Başlık 1 stiliyle biçimlendirilmiş bir paragrafı bir belgeden diğerine kopyalamak için, bir dizi şey dikkate alınmalıdır: Başlık 1 stilini kaynak belgeden hedef belgeye kopyalayın, paragrafı kopyalayın, klonlanan paragrafını hedef belgedeki doğru Başlık 1 stiline atıfta bulunacak şekilde güncelleyin. Stilin kopyalanması gerekiyorsa, tüm stilleri referanslar (style ve sonraki paragraf stiline göre) analiz edilmeli ve muhtemelen kopyalanmalıdır ve bu böyle devam eder. Microsoft Word liste tanımlarını metinden ayrı olarak sakladığından, madde işaretli veya numaralı paragrafları kopyalarken benzer sorunlar vardır.

bu[`NodeImporter`](./nodeimporter/)sınıf, içe aktarma sırasında "çeviri tablolarını" tutan bir bağlam gibidir. Kaynak and hedef belgelerdeki stiller ve listeler arasında doğru çeviri yapar.

### Örnekler

Bir belgenin içeriğinin başka bir belgedeki yer işaretine nasıl ekleneceğini gösterir.

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
/// Belirtilen düğümden sonra bir belgenin içeriğini ekler.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Bölümün gövdesindeki tüm blok düzeyindeki düğümler arasında dolaşın,
        // sonra bir bölümün son boş paragrafı olmayan her düğümü klonlayın ve ekleyin.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
