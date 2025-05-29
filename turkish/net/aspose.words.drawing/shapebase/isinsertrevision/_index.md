---
title: ShapeBase.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: .NET için Aspose.Words
description: ShapeBase'in IsInsertRevision özelliğinin izleme sırasında yapılan değişiklikleri belirleyerek Word belgelerinizi nasıl geliştirdiğini keşfedin. Düzenleme verimliliğinizi artırın!
type: docs
weight: 320
url: /tr/net/aspose.words.drawing/shapebase/isinsertrevision/
---
## ShapeBase.IsInsertRevision property

Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür.

```csharp
public bool IsInsertRevision { get; }
```

## Örnekler

Revizyon şekilleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Revizyonları izlemeyen bir satır içi şekil ekle, bu şeklin hiçbir şekilde bir revizyon olmamasını sağlar.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Revizyonları izlemeye başla ve ardından revizyon olacak başka bir şekil ekle.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Değişiklikleri izlerken o şekli kaldırdığımızdan,
// şekil belgede kalır ve silme revizyonu olarak sayılır.
// Bu düzeltmeyi kabul etmek şekli kalıcı olarak kaldıracak, reddetmek ise belgede kalmasını sağlayacaktır.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// Ve değişiklikleri izlerken başka bir şekil daha ekledik, bu yüzden bu şekil bir ekleme revizyonu olarak sayılacak.
// Bu revizyonu kabul etmek, bu şeklin revizyon olmayan bir belge olarak belgeye dahil edilmesine neden olacaktır.
// ve revizyonu reddetmek bu şekli kalıcı olarak kaldıracaktır.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
