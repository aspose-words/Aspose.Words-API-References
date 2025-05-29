---
title: CompositeNode.InsertAfter
linktitle: InsertAfter
articleTitle: InsertAfter
second_title: .NET için Aspose.Words
description: CompositeNode InsertAfter metodu ile düğümleri zahmetsizce ekleyin, veri yapınızın yönetimini geliştirin ve verimli düğüm yerleşimini garantileyin.
type: docs
weight: 150
url: /tr/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter&lt;T&gt; method

Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler.

```csharp
public T InsertAfter<T>(T newChild, Node refChild)
    where T : Node
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newChild | T | The[`Node`](../../node/) eklemek için. |
| refChild | Node | The[`Node`](../../node/) bu referans düğümüdür.*newChild* sonrasında yerleştirilir*refChild*. |

### Geri dönüş değeri

Eklenen düğüm.

## Notlar

Eğer*refChild* dır`hükümsüz` , ekler*newChild* çocuk düğümlerinin listesinin başında.

Eğer*newChild* Ağaçta zaten varsa, önce o kaldırılır.

Eklenen düğüm başka bir belgeden oluşturulduysa, kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. Daha sonra içe aktarılan düğüm geçerli belgeye eklenebilir.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
