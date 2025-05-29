---
title: NodeCollection Class
linktitle: NodeCollection
articleTitle: NodeCollection
second_title: .NET için Aspose.Words
description: Belge işlemede çeşitli düğüm türlerini verimli bir şekilde yönetmek için başvuracağınız çözüm olan Aspose.Words.NodeCollection sınıfını keşfedin. İş akışınızı bugün geliştirin!
type: docs
weight: 4890
url: /tr/net/aspose.words/nodecollection/
---
## NodeCollection class

Belirli bir türdeki düğümlerin bir koleksiyonunu temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Belirtilen dizindeki bir düğümü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondan ve belgeden tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizinde koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |

## Notlar

`NodeCollection` içerdiği düğümlerin sahibi değildir, bunun yerine belirtilen türdeki nodes düğümlerinin bir seçimidir, ancak düğümler ağaçta kendi üst düğümlerinin altında saklanır.

`NodeCollection` dizinli erişimi, yinelemeyi destekler ve ekleme ve kaldırma yöntemleri sağlar.

The`NodeCollection` koleksiyon "canlıdır", yani oluşturulduğu object düğümünün çocuklarında yapılan değişiklikler, tarafından döndürülen düğümlere hemen yansıtılır`NodeCollection` özellikleri ve yöntemleri.

`NodeCollection` tarafından iade edilir[`GetChildNodes`](../compositenode/getchildnodes/) ve ayrıca şu türdeki düğüm koleksiyonları için bir temel sınıf görevi görür:[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) vesaire.

`NodeCollection`"düz" olabilir ve yalnızca oluşturulduğu düğümün doğrudan alt öğelerini içerebilir veya "derin" olabilir ve tüm alt öğeleri içerebilir.

## Örnekler

Tüm metin kutusu şekillerinin resim şekilleriyle nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Ayrıca bakınız

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
