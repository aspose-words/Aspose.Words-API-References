---
title: GetChildNodes
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür.
type: docs
weight: 100
url: /tr/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| nodeType | NodeType | Seçilecek düğümlerin türünü belirtir. |
| isDeep | Boolean | Tüm alt düğümlerden özyinelemeli olarak seçim yapmak için true. Yalnızca en yakın alt öğeler arasından seçim yapmak için False. |

### Geri dönüş değeri

Belirtilen türdeki alt düğümlerin canlı koleksiyonu.

### Notlar

Bu yöntemle döndürülen düğümlerin koleksiyonu her zaman canlıdır.

Canlı bir koleksiyon her zaman belgeyle senkronize olur. Örneğin, siz bir belgedeki tüm bölümleri seçtiyseniz ve bölümleri silerek collection boyunca numaralandırdıysanız, bölüm belgeden kaldırıldığında hemen koleksiyondan kaldırılır.

### Örnekler

Bir belgenin tüm yorumlarının ve yanıtlarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Bir yorumun atası yoksa, yanıt türü bir yorumun aksine "üst düzey" bir yorumdur.
// Tüm üst düzey yorumları, olabilecek yanıtlarla birlikte yazdırın.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

Bir belgeden görüntülerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgeden şekil koleksiyonunu alın,
// ve bir görüntü ile her şeklin görüntü verilerini yerel dosya sistemine dosya olarak kaydedin.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Şekillerin görüntü verileri, birçok olası görüntü formatının görüntülerini içerebilir. 
        // Her resim için formatına göre otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Bir CompositeNode'un alt öğeleri koleksiyonunda alt düğümlerin nasıl ekleneceğini, güncelleneceğini ve silineceğini gösterir.

```csharp
Document doc = new Document();

// Varsayılan olarak boş bir belgenin bir paragrafı vardır.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Paragrafımız gibi bileşik düğümler, alt öğe olarak diğer bileşik ve satır içi düğümleri içerebilir.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Üç çalıştırma düğümü daha oluşturun.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Belge gövdesi, biz bunları bir bileşik düğüme ekleyene kadar bu çalıştırmaları görüntülemeyecektir.
// bu, ilk çalıştırmada yaptığımız gibi, belgenin düğüm ağacının bir parçasıdır.
// Eklediğimiz düğümlerin metin içeriklerinin nerede olduğunu belirleyebiliriz
// paragraftaki başka bir düğüme göre bir ekleme konumu belirterek belgede görünür.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// İkinci çalıştırmayı ilk çalıştırmanın önündeki paragrafa ekleyin.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// İlk çalıştırmadan sonra üçüncü çalıştırmayı ekleyin.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// İlk çalıştırmayı paragrafın alt düğüm koleksiyonunun başına ekleyin.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Mevcut alt düğümleri düzenleyip silerek çalıştırmanın içeriğini değiştirebiliriz.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ayrıca bakınız

* class [NodeCollection](../../nodecollection)
* enum [NodeType](../../nodetype)
* class [CompositeNode](../../compositenode)
* ad alanı [Aspose.Words](../../compositenode)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
