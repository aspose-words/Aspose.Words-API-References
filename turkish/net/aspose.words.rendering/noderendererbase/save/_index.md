---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: NodeRendererBase Save yöntem. Şekli bir görüntüye dönüştürür ve bir dosyaya kaydeder C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_1}

Şekli bir görüntüye dönüştürür ve bir dosyaya kaydeder.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resim dosyasının adı. Belirtilen ada sahip bir dosya zaten mevcutsa mevcut dosyanın üzerine yazılır. |
| saveOptions | ImageSaveOptions | Şeklin nasıl oluşturulacağını ve kaydedileceğini denetleyen seçenekleri belirtir. Olabilir`hükümsüz`. |

## Örnekler

Bir Office Math nesnesinin yerel dosya sistemindeki bir görüntü dosyasına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Değiştirmek üzere düğüm oluşturucunun "Kaydet" yöntemine iletilecek bir "ImageSaveOptions" nesnesi oluşturun
// OfficeMath düğümünü bir görüntüye nasıl dönüştürdüğü.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Nesneyi orijinal boyutunun beş katına çıkarmak için "Ölçek" özelliğini 5'e ayarlayın.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Şekli bir görüntüye dönüştürür ve bir akışa kaydeder.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Şeklin görüntüsünün kaydedileceği akış. |
| saveOptions | ImageSaveOptions | Şeklin nasıl oluşturulacağını ve kaydedileceğini denetleyen seçenekleri belirtir. Olabilir`hükümsüz` . Eğer bu ise`hükümsüz`görüntü PNG formatında kaydedilecektir. |

## Örnekler

Şekilleri yerel dosya sistemindeki dosyalara aktarmak için şekil oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Belgede 2 alt şekle sahip bir grup şekli de dahil olmak üzere 7 şekil var.
// Her şekli yerel dosya sistemindeki bir görüntü dosyasına dönüştüreceğiz
// görünümleri olmadığı için grup şekillerini göz ardı ediyoruz.
// Bu 6 adet resim dosyası üretecektir.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
