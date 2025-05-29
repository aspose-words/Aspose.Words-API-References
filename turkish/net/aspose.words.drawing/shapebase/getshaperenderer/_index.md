---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: .NET için Aspose.Words
description: Şekilleri zahmetsizce resim olarak oluşturmak ve işlemek, tasarım projelerinizi kolaylıkla geliştirmek için ShapeBase GetShapeRenderer metodunu keşfedin.
type: docs
weight: 670
url: /tr/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Bu şekli bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Geri dönüş değeri

Bu şeklin işleyici nesnesi.

## Notlar

Bu yöntem yalnızca şunu çağırır:[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) constructor'ı kullanın ve bu nesneyi parametre olarak pass olarak geçirin.

## Örnekler

Şekilleri yerel dosya sistemindeki dosyalara aktarmak için şekil oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Belgede 2 alt şekle sahip bir grup şekli de dahil olmak üzere 7 şekil var.
// Her şekli yerel dosya sistemindeki bir görüntü dosyasına dönüştüreceğiz
// grup şekillerini görmezden gelirken, görünümleri olmadığı için.
// Bu 6 adet resim dosyası üretecektir.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Ayrıca bakınız

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
