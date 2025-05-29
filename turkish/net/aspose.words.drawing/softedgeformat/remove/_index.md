---
title: SoftEdgeFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: SoftEdgeFormat Remove yöntemiyle SoftEdgeFormat'ı ana nesnenizden zahmetsizce kaldırın. En iyi sonuçlar için tasarımınızı kolaylaştırın!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat.Remove method

Kaldırır[`SoftEdgeFormat`](../) ana nesneden.

```csharp
public void Remove()
```

## Örnekler

Görüntü çözünürlüğü için sınır belirlemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Yumuşak kenar biçimlendirmesinin nasıl yapılacağını gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Şekle yumuşak kenar uygulayın.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Yumuşak kenarlı dikdörtgen şekilli belgeyi yükleyin.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Yumuşak kenar yarıçapını kontrol edin.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Şeklin yumuşak kenarını çıkarın.
softEdgeFormat.Remove();

// Kaldırılan yumuşak kenarın yarıçapını kontrol edin.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Ayrıca bakınız

* class [SoftEdgeFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
