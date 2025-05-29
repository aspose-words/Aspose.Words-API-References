---
title: OleFormat.IsLink
linktitle: IsLink
articleTitle: IsLink
second_title: .NET için Aspose.Words
description: OleFormat IsLink özelliğini keşfedin. Sorunsuz veri entegrasyonu ve yönetimi için OLE nesnenizin SourceFullName ile bağlantılı olup olmadığını kolayca kontrol edin.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/oleformat/islink/
---
## OleFormat.IsLink property

Geri Döndürür`doğru` OLE nesnesi bağlıysa (ne zaman[`SourceFullName`](../sourcefullname/) belirtilmiştir).

```csharp
public bool IsLink { get; }
```

## Örnekler

Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Microsoft Visio çizimini OLE nesnesi olarak belgeye göm.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Yerel dosya sistemindeki dosyaya bir bağlantı ekle ve bunu bir simge olarak görüntüle.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// OLE nesnelerinin eklenmesi, bu nesneleri depolayan şekiller oluşturur.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Bir şekil bir OLE nesnesi içeriyorsa, geçerli bir "OleFormat" özelliğine sahip olacaktır.
// şeklin bazı yönlerini doğrulamak için kullanabiliriz.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// Eğer nesne OLE verisi içeriyorsa, bir akış kullanarak ona erişebiliriz.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Ayrıca bakınız

* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
