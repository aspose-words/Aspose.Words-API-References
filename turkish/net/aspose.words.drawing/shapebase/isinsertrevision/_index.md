---
title: ShapeBase.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words for .NET
description: ShapeBase IsInsertRevision mülk. Bu nesne Microsoft Worde değişiklik izleme etkinken eklenmişse doğru değerini döndürür C#'da.
type: docs
weight: 300
url: /tr/net/aspose.words.drawing/shapebase/isinsertrevision/
---
## ShapeBase.IsInsertRevision property

Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür.

```csharp
public bool IsInsertRevision { get; }
```

## Örnekler

Revizyon şekilleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Düzeltmeleri izlemeden satır içi bir şekil ekleyin; bu, bu şeklin herhangi bir türde revizyon olmamasını sağlar.
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

// Değişiklikleri takip ederken o şekli kaldırdığımız için,
// şekil belgede kalır ve revizyon silme olarak sayılır.
// Bu düzeltmeyi kabul etmek şekli kalıcı olarak kaldıracak, reddetmek ise onu belgede tutacaktır.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// Ve değişiklikleri izlerken başka bir şekil ekledik, böylece bu şekil bir ekleme revizyonu olarak sayılacaktır.
// Bu revizyonun kabul edilmesi, bu şeklin revizyon dışı olarak belgeye asimile edilmesini sağlayacaktır,
// ve düzeltmenin reddedilmesi bu şekli kalıcı olarak kaldıracaktır.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
