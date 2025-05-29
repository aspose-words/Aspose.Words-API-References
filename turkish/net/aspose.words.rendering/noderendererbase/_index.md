---
title: NodeRendererBase Class
linktitle: NodeRendererBase
articleTitle: NodeRendererBase
second_title: .NET için Aspose.Words
description: Belge işlemede etkili Shape ve OfficeMath işleme için temeliniz olan Aspose.Words.Rendering.NodeRendererBase sınıfını keşfedin.
type: docs
weight: 5280
url: /tr/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Temel sınıf[`ShapeRenderer`](../shaperenderer/) Ve[`OfficeMathRenderer`](../officemathrenderer/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Şekillerle Çalışma](https://docs.aspose.com/words/net/working-with-shapes/) belgeleme makalesi.

```csharp
public abstract class NodeRendererBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Şeklin gerçek sınırlarını noktalar halinde alır. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Şeklin opak sınırlarını noktalar halinde alır. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Şeklin gerçek boyutunu noktalar halinde alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(*float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını piksel cinsinden hesaplar. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(*float, float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını piksel cinsinden hesaplar. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(*float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(*float, float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(*float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Şekli birGraphics nesnesi belirtilen bir ölçeğe göre. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Şekli birGraphics nesnesini belirtilen bir boyuta ayarlayın. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Şekli bir görüntüye dönüştürür ve bir akışa kaydeder. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Şekli bir SVG görüntüsüne dönüştürür ve bir akışa kaydeder. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Şekli bir görüntüye dönüştürür ve bir dosyaya kaydeder. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_3)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Şekli bir SVG görüntüsüne dönüştürür ve bir dosyaya kaydeder. |

## Örnekler

Şekillerin nasıl ölçüleceğini ve ölçeklendirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// OfficeMath nesnesinin render edildiğinde oluşturacağı görüntünün boyutunu doğrulayın.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Şeffaf parçalara sahip şekiller "OpaqueBoundsInPoints" özelliklerinde farklı değerler içerebilir.
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Belirli bir DPI'a doğrusal ölçeklemeyle şeklin boyutunu piksel cinsinden alın.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Şeklin boyutunu piksel cinsinden al, ancak yatay ve dikey boyutlar için farklı DPI'lar kullan.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Burada da opak sınırlar değişebilir.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)
