---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: .NET için Aspose.Words
description: NodeRendererBase Save metodunu keşfedin. Şekilleri kolayca görüntü olarak işleyin ve kusursuz entegrasyon ve gelişmiş üretkenlik için dosyalara kaydedin.
type: docs
weight: 90
url: /tr/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

Şekli bir görüntüye dönüştürür ve bir dosyaya kaydeder.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Görüntü dosyasının adı. Belirtilen ada sahip bir dosya zaten varsa, var olan dosyanın üzerine yazılır. |
| saveOptions | ImageSaveOptions | Şeklin nasıl oluşturulacağını ve kaydedileceğini kontrol eden seçenekleri belirtir.`hükümsüz`. |

## Örnekler

Office Math nesnesinin yerel dosya sisteminde bir görüntü dosyasına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Düğüm oluşturucusunun "Kaydet" yöntemine geçirilecek ve değiştirilecek bir "ImageSaveOptions" nesnesi oluşturun
// OfficeMath düğümünü bir görüntüye nasıl dönüştürdüğü.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Nesneyi orijinal boyutunun beş katına çıkarmak için "Ölçek" özelliğini 5 olarak ayarlayın.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

Şekli bir SVG görüntüsüne dönüştürür ve bir dosyaya kaydeder.

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Görüntü dosyasının adı. Belirtilen ada sahip bir dosya zaten varsa, var olan dosyanın üzerine yazılır. |
| saveOptions | SvgSaveOptions | Şeklin nasıl oluşturulacağını ve kaydedileceğini kontrol eden seçenekleri belirtir.`hükümsüz`. |

## Örnekler

Office matematiği oluştururken kaydetme seçeneklerinin nasıl geçileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Ayrıca bakınız

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
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
| saveOptions | ImageSaveOptions | Şeklin nasıl oluşturulacağını ve kaydedileceğini kontrol eden seçenekleri belirtir.`hükümsüz` . Eğer bu ise`hükümsüz`resim PNG formatında kaydedilecektir. |

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

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

Şekli bir SVG görüntüsüne dönüştürür ve bir akışa kaydeder.

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Şeklin SVG görüntüsünün kaydedileceği akış. |
| saveOptions | SvgSaveOptions | Şeklin nasıl oluşturulacağını ve kaydedileceğini kontrol eden seçenekleri belirtir.`hükümsüz` . Eğer bu ise`hükümsüz`, resim varsayılan seçeneklerle kaydedilecektir. |

## Örnekler

Office matematiği oluştururken kaydetme seçeneklerinin nasıl geçileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Ayrıca bakınız

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
