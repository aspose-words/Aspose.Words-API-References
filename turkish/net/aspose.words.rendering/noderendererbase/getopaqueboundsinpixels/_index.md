---
title: GetOpaqueBoundsInPixels
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar.
type: docs
weight: 50
url: /tr/net/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## GetOpaqueBoundsInPixels(float, float) {#getopaqueboundsinpixels}

Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float dpi)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| scale | Single | Yakınlaştırma faktörü (1.0, %100'dür). |
| dpi | Single | Noktalardan piksellere (inç başına nokta) dönüştürme çözünürlüğü. |

### Geri dönüş değeri

Şeklin piksel cinsinden opak dikdörtgeni.

### Notlar

Bu yöntem dönüştürür[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) piksel cinsinden dikdörtgene dönüştürün ve şeklin yalnızca opak kısmıyla şekli oluşturmak için bir bitmap oluşturmak istediğinizde kullanışlıdır.

### Örnekler

Şekillerin nasıl ölçüleceğini ve ölçekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Oluşturduğumuzda OfficeMath nesnesinin oluşturacağı görüntünün boyutunu doğrulayın.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Saydam kısımlara sahip şekiller, "OpaqueBoundsInPoints" özelliklerinde farklı değerler içerebilir.
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Belirli bir DPI'ye doğrusal ölçekleme ile şekil boyutunu piksel olarak alın.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Şekil boyutunu piksel olarak alın, ancak yatay ve dikey boyutlar için farklı bir DPI ile.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Opak sınırlar burada da değişebilir.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Ayrıca bakınız

* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../noderendererbase/)
* toplantı [Aspose.Words](../../../)

---

## GetOpaqueBoundsInPixels(float, float, float) {#getopaqueboundsinpixels_1}

Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını piksel cinsinden hesaplar.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| scale | Single | Yakınlaştırma faktörü (1.0, %100'dür). |
| horizontalDpi | Single | Noktalardan piksellere (inç başına nokta) dönüştürülecek yatay çözünürlük. |
| verticalDpi | Single | Noktalardan piksellere (inç başına nokta) dönüştürülecek dikey çözünürlük. |

### Geri dönüş değeri

Şeklin piksel cinsinden opak dikdörtgeni.

### Notlar

Bu yöntem dönüştürür[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) piksel cinsinden dikdörtgene dönüştürün ve şeklin yalnızca opak kısmıyla şekli oluşturmak için bir bitmap oluşturmak istediğinizde kullanışlıdır.

### Örnekler

Şekillerin nasıl ölçüleceğini ve ölçekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Oluşturduğumuzda OfficeMath nesnesinin oluşturacağı görüntünün boyutunu doğrulayın.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Saydam kısımlara sahip şekiller, "OpaqueBoundsInPoints" özelliklerinde farklı değerler içerebilir.
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Belirli bir DPI'ye doğrusal ölçekleme ile şekil boyutunu piksel olarak alın.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Şekil boyutunu piksel olarak alın, ancak yatay ve dikey boyutlar için farklı bir DPI ile.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Opak sınırlar burada da değişebilir.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Ayrıca bakınız

* class [NodeRendererBase](../)
* ad alanı [Aspose.Words.Rendering](../../noderendererbase/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
