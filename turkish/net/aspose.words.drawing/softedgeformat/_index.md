---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: .NET için Aspose.Words
description: Belgelerinizi profesyonel bir görünüm için çarpıcı yumuşak kenar efektleriyle geliştirmek üzere Aspose.Words.Drawing.SoftEdgeFormat sınıfını keşfedin.
type: docs
weight: 1710
url: /tr/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Bir nesnenin yumuşak kenar biçimlendirmesini temsil eder.

```csharp
public class SoftEdgeFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Yumuşak kenar efektinin yarıçapının uzunluğunu noktalar (pt) cinsinden temsil eden bir çift değer alır veya ayarlar. Varsayılan değer 0.0'dır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Kaldırır`SoftEdgeFormat` ana nesneden. |

## Notlar

Kullanın[`SoftEdge`](../shapebase/softedge/) Bir nesnenin yumuşak kenar özelliklerine erişmek için özellik. Örnekleri oluşturmazsınız`SoftEdgeFormat` sınıfa doğrudan.

## Örnekler

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
