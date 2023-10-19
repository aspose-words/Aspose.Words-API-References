---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: CompositeNode GetEnumerator yöntem. Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar.

```csharp
public IEnumerator<Node> GetEnumerator()
```

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
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
