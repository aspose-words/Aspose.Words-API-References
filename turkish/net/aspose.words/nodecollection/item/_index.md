---
title: NodeCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: NodeCollection Item özelliğiyle herhangi bir düğüme zahmetsizce erişin. Sorunsuz veri yönetimi ve gelişmiş performans için düğümleri dizine göre hızla alın.
type: docs
weight: 20
url: /tr/net/aspose.words/nodecollection/item/
---
## NodeCollection indexer

Belirtilen dizindeki bir düğümü alır.

```csharp
public Node this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Düğüm koleksiyonuna ait bir indeks. |

## Notlar

Endeks sıfır bazlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi belirtir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

Eğer indeks listedeki öğe sayısından büyük veya eşitse, bu boş bir referans döndürür.

Eğer indeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu durum boş bir referans döndürür.

## Örnekler

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

### Ayrıca bakınız

* class [Node](../../node/)
* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
