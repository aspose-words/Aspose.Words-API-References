---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: .NET için Aspose.Words
description: ShapeBase'i keşfedin. Belgelerinizdeki dekoratif özellikleri kolayca yönetin. Benzersiz şekil tasarımları için bayraklar ayarlayarak görsel çekiciliği artırın.
type: docs
weight: 260
url: /tr/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Şeklin belgede dekoratif olup olmadığını belirten bayrağı alır veya ayarlar.

```csharp
public bool IsDecorative { get; set; }
```

## Notlar

Şeklin boş olmadığına dikkat edin[`AlternativeText`](../alternativetext/) dekoratif olamaz.

## Örnekler

Şeklin dekoratif olarak nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// "AlternativeText" boş değilse şekil dekoratif olamaz.
// Bu yüzden değerimiz 'false' olarak değişti.
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Dekoratif amaçlı yeni bir şekil oluştur.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
