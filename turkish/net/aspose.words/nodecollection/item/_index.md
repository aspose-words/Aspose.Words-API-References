---
title: NodeCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: NodeCollection Item mülk. Verilen dizindeki bir düğümü alır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/nodecollection/item/
---
## NodeCollection indexer

Verilen dizindeki bir düğümü alır.

```csharp
public Node this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Düğümlerin koleksiyonuna ilişkin bir dizin. |

## Notlar

Endeks sıfır bazlıdır.

Negatif dizinlere izin verilir ve koleksiyonun arkasından erişimi belirtir. Örneğin -1 son öğe anlamına gelir, -2 sondan önceki ikinci öğe anlamına gelir ve bu şekilde devam eder.

Dizin listedeki öğe sayısından büyük veya ona eşitse bu, boş bir başvuru döndürür.

Dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse bu, boş bir başvuru döndürür.

## Örnekler

Bileşik bir düğümün alt düğüm koleksiyonunda nasıl geçiş yapılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına alt düğümler olarak iki işlem ve bir şekil ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId'in bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün ömrü boyunca mevcut olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın yakın alt öğelerinin toplanması yoluyla yineleme yapın,
// ve içinde bulduğumuz tüm sayıları veya şekilleri yazdırıyoruz.
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
