---
title: CompositeNode.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: .NET için Aspose.Words
description: CompositeNode GetChildNodes yöntemini keşfedin; gelişmiş performans için belirttiğiniz türe göre uyarlanmış canlı bir alt düğüm koleksiyonunu zahmetsizce alın.
type: docs
weight: 110
url: /tr/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| nodeType | NodeType | Seçilecek düğüm türünü belirtir. |
| isDeep | Boolean | `doğru` tüm alt düğümlerden yinelemeli olarak seçim yapmak için; `YANLIŞ` sadece yakın çocuklar arasından seçim yapmak. |

### Geri dönüş değeri

Belirtilen türdeki alt düğümlerin canlı koleksiyonu.

## Notlar

Bu yöntemle döndürülen düğüm koleksiyonu her zaman canlıdır.

Canlı bir koleksiyon her zaman belgeyle senkronizedir. Örneğin, you bir belgedeki tüm bölümleri seçtiyseniz ve bölümleri silerek collection boyunca numaralandırırsanız, bölüm belgeden kaldırıldığında hemen koleksiyondan kaldırılır.

## Örnekler

Bir belgenin tüm yorumlarının ve bunların yanıtlarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Eğer bir yorumun bir atası yoksa, bu bir yanıt türü yorumun aksine "en üst düzey" yorumdur.
// Tüm üst düzey yorumları ve bunlara ait tüm yanıtları yazdır.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
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

Bir belgeden resimlerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Şekil koleksiyonunu belgeden al,
// ve her şeklin görüntü verisini, görüntü içeren bir dosya olarak yerel dosya sistemine kaydeder.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Şekillerin görüntü verileri birçok olası görüntü formatındaki görüntüleri içerebilir.
        // Her bir resim için, formatına bağlı olarak otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Bir bileşik düğümün alt düğüm koleksiyonunda nasıl dolaşılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına iki çalışma ve bir şekil alt düğüm olarak ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId' öğesinin bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün yaşam süresi boyunca var olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın hemen altındaki alt öğelerin koleksiyonunda yineleme yapın,
// ve içinde bulduğumuz herhangi bir koşuyu veya şekli yazdırırız.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

CompositeNode'un alt düğüm koleksiyonuna alt düğümlerin nasıl ekleneceğini, güncelleneceğini ve silineceğini gösterir.

```csharp
Document doc = new Document();

// Boş bir belgenin varsayılan olarak bir paragrafı vardır.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Paragrafımızdaki gibi bileşik düğümler, çocuk olarak başka bileşik ve satır içi düğümler içerebilir.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Üç tane daha çalıştırma düğümü oluştur.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Belge gövdesi, bunları bileşik bir düğüme ekleyene kadar bu çalışmaları görüntülemeyecektir
// bu, ilk çalıştırmada yaptığımız gibi, belgenin düğüm ağacının bir parçasıdır.
// Eklediğimiz düğümlerin metin içeriklerinin nereye gideceğini belirleyebiliriz
// paragraftaki başka bir düğüme göre bir ekleme konumu belirtilerek belgede görünür.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// İkinci çalışmayı ilk çalışmanın önündeki paragrafa ekle.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// İlk çalıştırmadan sonra üçüncü çalıştırmayı ekle.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// İlk çalışmayı paragrafın alt düğüm koleksiyonunun başına ekle.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Mevcut alt düğümleri düzenleyerek ve silerek çalıştırmanın içeriğini değiştirebiliriz.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ayrıca bakınız

* class [NodeCollection](../../nodecollection/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
