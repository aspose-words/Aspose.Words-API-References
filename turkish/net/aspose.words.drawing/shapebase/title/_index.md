---
title: ShapeBase.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: ShapeBase Title mülk. Geçerli şekil nesnesinin başlığını başlığını alır veya ayarlar C#'da.
type: docs
weight: 530
url: /tr/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Geçerli şekil nesnesinin başlığını (başlığını) alır veya ayarlar.

```csharp
public string Title { get; set; }
```

## Notlar

Varsayılan boş dizedir.

Olamaz`hükümsüz`, ancak boş bir dize olabilir.

## Örnekler

Bir şeklin başlığının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir şekil oluşturun, ona bir başlık verin ve ardından onu belgeye ekleyin.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// Başlığı olan bir şekle sahip bir belgeyi kaydettiğimizde,
// Aspose.Words bu başlığı şeklin Alternatif Metnine kaydedecektir.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
