---
title: ShapeBase.IsInsertRevision
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Bu nesne değişiklik izleme etkinken Microsoft Worde eklendiyse true değerini döndürür.
type: docs
weight: 290
url: /tr/net/aspose.words.drawing/shapebase/isinsertrevision/
---
## ShapeBase.IsInsertRevision property

Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür.

```csharp
public bool IsInsertRevision { get; }
```

### Örnekler

Revizyon şekilleri ile nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Revizyonları izlemeden satır içi bir şekil ekleyin; bu, bu şekli herhangi bir revizyon olmaktan çıkaracaktır.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Revizyonları izlemeye başlayın ve ardından revizyon olacak başka bir şekil ekleyin.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Değişiklikleri takip ederken bu şekli kaldırdığımız için,
// şekil belgede kalır ve bir silme revizyonu olarak sayılır.
// Bu revizyonu kabul etmek şekli kalıcı olarak kaldıracak ve reddetmek belgede kalmasını sağlayacaktır.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// Ve değişiklikleri izlerken başka bir şekil ekledik, böylece şekil bir ekleme revizyonu olarak sayılacak.
// Bu revizyonu kabul etmek, bu şekli belgeye revizyonsuz olarak asimile edecektir,
// ve revizyonu reddetmek bu şekli kalıcı olarak kaldıracaktır.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


