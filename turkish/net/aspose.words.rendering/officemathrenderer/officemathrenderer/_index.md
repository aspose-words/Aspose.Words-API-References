---
title: OfficeMathRenderer
linktitle: OfficeMathRenderer
articleTitle: OfficeMathRenderer
second_title: .NET için Aspose.Words
description: OfficeMathRenderer oluşturucusu ile dinamik matematik gösterimlerini zahmetsizce oluşturun. Belgelerinizi kusursuz matematiksel işleme ile geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.rendering/officemathrenderer/officemathrenderer/
---
## OfficeMathRenderer constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public OfficeMathRenderer(OfficeMath math)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| math | OfficeMath | The[`OfficeMath`](../../../aspose.words.math/officemath/) işlemek istediğiniz nesne. |

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

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [OfficeMathRenderer](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
