---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: .NET için Aspose.Words
description: Tasarımlarınızı, pürüzsüz, yumuşak kenar biçimlendirmesi için ShapeBase SoftEdge ile geliştirin. Görsellerinizi zahmetsizce yükseltin ve her projede öne çıkın!
type: docs
weight: 550
url: /tr/net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

Şekil için yumuşak kenar biçimlendirmesi alır.

```csharp
public SoftEdgeFormat SoftEdge { get; }
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

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
