---
title: ShapeBase.IsMoveToRevision
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. İadelerdoğru bu nesne Microsoft Wordde değişiklik izleme etkinken taşınmışsa eklenmişse.
type: docs
weight: 330
url: /tr/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse).

```csharp
public bool IsMoveToRevision { get; }
```

### Örnekler

Revizyon şekillerini taşımanın nasıl tanımlanacağını gösterir.

```csharp
// Düzeltmeyi taşıma, belge gövdesindeki bir öğeyi Microsoft Word'de kesip yapıştırarak taşımamızdır.
//değişiklikleri takip ediyoruz. Böyle bir metin hareketine satır içi bir şekil katarsak o şekil de bir revizyon olacaktır.
// Kayan şekilleri kopyalayıp yapıştırmak veya taşımak, taşıma revizyonları oluşturmaz.
Document doc = new Document(MyDir + "Revision shape.docx");

// Revizyonları taşıma, "Şuraya Taşı" ve "Şuraya Taşı" revizyon çiftlerinden oluşur. Bu belgede tek bir biçimde taşındık,
// ancak taşıma revizyonunu kabul edene veya reddedene kadar bu şeklin iki örneği olacaktır.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Bu, varış yerindeki şekil olan "Şuraya Taşı" revizyonudur.
// Eğer revizyonu kabul edersek bu "Taşı" revizyon şekli kaybolacaktır,
// ve "Şuradan taşı" revizyon şekli kalacaktır.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Bu, şeklin orijinal konumundaki "Taşı" revizyonudur.
// Eğer revizyonu kabul edersek bu "Şuradan taşı" revizyon şekli kaybolacaktır,
// ve "Şuraya Taşı" revizyon şekli kalacaktır.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


