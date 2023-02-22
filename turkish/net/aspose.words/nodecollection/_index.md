---
title: Class NodeCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.NodeCollection sınıf. Belirli bir türdeki düğümler koleksiyonunu temsil eder.
type: docs
weight: 3960
url: /tr/net/aspose.words/nodecollection/
---
## NodeCollection class

Belirli bir türdeki düğümler koleksiyonunu temsil eder.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Verilen dizindeki bir düğümü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Koleksiyonda bir düğüm olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" stili yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Belirtilen dizindeki koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |

### Notlar

**Düğüm Koleksiyonu** içerdiği düğümlere sahip değildir, bunun yerine yalnızca belirtilen türdeki düğümler 'nin bir seçimidir, ancak düğümler ağaçta ilgili üst düğümleri altında depolanır.

**Düğüm Koleksiyonu**dizine alınmış erişimi, yinelemeyi destekler ve ekleme ve kaldırma yöntemleri sağlar.

bu **Düğüm Koleksiyonu** koleksiyon "canlı"dır, yani nesnenin oluşturulduğu object düğümünün çocuklarında yapılan değişiklikler, anında döndürülen düğümlere yansıtılır. **Düğüm Koleksiyonu** özellikleri ve yöntemleri.

**Düğüm Koleksiyonu** tarafından iade edilir[`GetChildNodes`](../compositenode/getchildnodes/) ve ayrıca aşağıdaki gibi yazılan düğüm koleksiyonları için bir temel sınıf görevi görür[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) vb.

**Düğüm Koleksiyonu** "düz" olabilir ve yalnızca oluşturulduğu düğümünün doğrudan alt öğelerini içerebilir veya "derin" olabilir ve tüm alt öğeleri içerebilir.

### Örnekler

Tüm metin kutusu şekillerinin görüntü şekilleriyle nasıl değiştirileceğini gösterir.

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


