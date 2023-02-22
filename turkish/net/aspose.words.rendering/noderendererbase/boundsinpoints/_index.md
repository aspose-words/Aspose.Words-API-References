---
title: NodeRendererBase.BoundsInPoints
second_title: Aspose.Words for .NET API Referansı
description: NodeRendererBase mülk. Şeklin gerçek sınırlarını nokta olarak alır.
type: docs
weight: 10
url: /tr/net/aspose.words.rendering/noderendererbase/boundsinpoints/
---
## NodeRendererBase.BoundsInPoints property

Şeklin gerçek sınırlarını nokta olarak alır.

```csharp
public RectangleF BoundsInPoints { get; }
```

### Notlar

Bu özellik, şeklin gerçek (sayfada işlendiği gibi) sınırlayıcı kutusunu döndürür. Sınırlar, (varsa) şekil döndürmeyi hesaba katar.

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


