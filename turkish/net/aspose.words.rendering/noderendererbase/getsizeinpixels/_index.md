---
title: NodeRendererBase.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: .NET için Aspose.Words
description: Yakınlaştırma faktörü ve çözünürlüğe göre şekil boyutlarını piksel cinsinden doğru bir şekilde hesaplamak için NodeRendererBase GetSizeInPixels yöntemini keşfedin. Tasarımlarınızı optimize edin!
type: docs
weight: 60
url: /tr/net/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| scale | Single | Yakınlaştırma faktörü (1.0 = %100). |
| dpi | Single | Noktadan piksele (inç başına nokta) dönüştürülecek çözünürlük (yatay ve dikey). |

### Geri dönüş değeri

Şeklin piksel cinsinden boyutu.

## Notlar

Bu yöntem dönüştürür[`SizeInPoints`](../sizeinpoints/) piksel cinsinden boyuta dönüştürür ve şekli bitmap üzerine düzgün bir şekilde işlemek için bir bitmap oluşturmak istediğinizde kullanışlıdır.

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

* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu piksel cinsinden hesaplar.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| scale | Single | Yakınlaştırma faktörü (1.0 = %100). |
| horizontalDpi | Single | Noktadan piksele (inç başına nokta) dönüştürülecek yatay çözünürlük. |
| verticalDpi | Single | Noktadan piksele (inç başına nokta) dönüştürülecek dikey çözünürlük. |

### Geri dönüş değeri

Şeklin piksel cinsinden boyutu.

## Notlar

Bu yöntem dönüştürür[`SizeInPoints`](../sizeinpoints/) piksel cinsinden boyuta dönüştürür ve şekli bitmap üzerine düzgün bir şekilde işlemek için bir bitmap oluşturmak istediğinizde kullanışlıdır.

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

* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
