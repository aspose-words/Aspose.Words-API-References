---
title: NodeRendererBase.OpaqueBoundsInPoints
linktitle: OpaqueBoundsInPoints
articleTitle: OpaqueBoundsInPoints
second_title: .NET için Aspose.Words
description: Tasarım hassasiyetinizi ve verimliliğinizi artırmak için noktalardaki şekil sınırlarına kolayca erişmek amacıyla NodeRendererBase OpaqueBoundsInPoints özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.rendering/noderendererbase/opaqueboundsinpoints/
---
## NodeRendererBase.OpaqueBoundsInPoints property

Şeklin opak sınırlarını noktalar halinde alır.

```csharp
public RectangleF OpaqueBoundsInPoints { get; }
```

## Notlar

Bu özellik şeklin opak (yani şeklin şeffaf kısımları göz ardı edilir) sınırlayıcı kutusunu döndürür. Sınırlar şeklin dönüşünü hesaba katar.

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
