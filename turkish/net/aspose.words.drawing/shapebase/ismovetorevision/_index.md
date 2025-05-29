---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: .NET için Aspose.Words
description: ShapeBase'in IsMoveToRevision özelliğinin, düzenlemeler sırasında nesne hareketlerini sorunsuz bir şekilde izleyerek Microsoft Word deneyiminizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 350
url: /tr/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse).

```csharp
public bool IsMoveToRevision { get; }
```

## Örnekler

Taşıma revizyon şekillerinin nasıl tanımlanacağını gösterir.

```csharp
// Bir taşıma revizyonu, bir öğeyi Microsoft Word'de kesip yapıştırarak belge gövdesinde taşıdığımız zamandır.
// değişiklikleri izleme. Böyle bir metin hareketine satır içi bir şekil dahil edersek, bu şekil de bir revizyon olacaktır.
// Kayan şekillerin kopyalanıp yapıştırılması veya taşınması taşıma revizyonları oluşturmaz.
Document doc = new Document(MyDir + "Revision shape.docx");

// Revizyonları taşıma, "Şuradan taşı" ve "Şuraya taşı" revizyon çiftlerinden oluşur. Bu belgede tek bir şekilde taşıdık,
// ancak taşıma revizyonunu kabul edene veya reddedene kadar, bu şeklin iki örneği olacak.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Bu, varış noktasındaki şeklin "Taşınacağı Yer" revizyonudur.
// Revizyonu kabul edersek, bu "Taşı" revizyon şekli kaybolacaktır,
// ve "Taşı" revizyon şekli aynı kalacaktır.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Bu, şeklin orijinal konumunda olduğu "Şuradan taşı" revizyonudur.
// Revizyonu kabul edersek, bu "Revizyondan taşı" şekli kaybolacaktır,
// ve "Taşı" revizyon şekli aynı kalacaktır.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
