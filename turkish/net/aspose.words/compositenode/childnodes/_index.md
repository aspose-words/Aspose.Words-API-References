---
title: CompositeNode.ChildNodes
second_title: Aspose.Words for .NET API Referansı
description: CompositeNode mülk. Bu düğümün tüm acil alt düğümlerini alır.
type: docs
weight: 10
url: /tr/net/aspose.words/compositenode/childnodes/
---
## CompositeNode.ChildNodes property

Bu düğümün tüm acil alt düğümlerini alır.

```csharp
public NodeCollection ChildNodes { get; }
```

### Notlar

Not,`ChildNodes` aramakla eşdeğerdir`GetChildNodes(NodeType.Any, yanlış)` ve her erişildiğinde yeni bir koleksiyon oluşturur ve döndürür.

Alt düğüm yoksa, bu özellik boş bir koleksiyon döndürür.

### Örnekler

Bileşik bir düğümün alt düğüm koleksiyonunda nasıl geçileceğini gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına alt düğümler olarak iki işlem ve bir şekil ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId' bir çıktı dosyasına kaydedilmediğini ve yalnızca düğüm ömrü boyunca var olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın acil alt öğeleri koleksiyonunu yineleyin,
// ve içinde bulduğumuz tüm koşuları veya şekilleri yazdırın.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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
    }
```

### Ayrıca bakınız

* class [NodeCollection](../../nodecollection/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../compositenode/)
* toplantı [Aspose.Words](../../../)


