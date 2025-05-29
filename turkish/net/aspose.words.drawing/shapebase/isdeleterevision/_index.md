---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: .NET için Aspose.Words
description: ShapeBase IsDeleteRevision özelliğini keşfedin, Microsoft Word'de gelişmiş belge yönetimi için değişiklik izleme etkinleştirildiğinde nesnenin silinmesini nasıl gösterdiğini öğrenin.
type: docs
weight: 270
url: /tr/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür.

```csharp
public bool IsDeleteRevision { get; }
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
