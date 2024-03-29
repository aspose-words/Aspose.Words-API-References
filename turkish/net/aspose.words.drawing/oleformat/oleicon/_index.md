---
title: OleFormat.OleIcon
linktitle: OleIcon
articleTitle: OleIcon
second_title: Aspose.Words for .NET
description: OleFormat OleIcon mülk. OLE nesnesinin çizim yönünü alır. Ne zamandoğru OLE nesnesi bir simge olarak görüntülenir. Ne zamanYANLIŞ OLE nesnesi content. olarak görüntülenir C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

OLE nesnesinin çizim yönünü alır. Ne zaman`doğru` OLE nesnesi bir simge olarak görüntülenir. Ne zaman`YANLIŞ` OLE nesnesi content. olarak görüntülenir.

```csharp
public bool OleIcon { get; }
```

## Notlar

Aspose.Words karışıklığı önlemek için bu özelliğin ayarlanmasına izin vermez. Aspose.Words'de çizim boyutunu değiştirebilseydiniz , Microsoft Word, siz Microsoft Word'de OLE nesnesini düzenleyene veya güncelleyene kadar OLE nesnesini orijinal çizim boyutunda görüntülemeye devam ederdi.

## Örnekler

Bağlı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Microsoft Visio çizimini belgeye OLE nesnesi olarak gömün.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Yerel dosya sistemindeki dosyaya bir bağlantı ekleyin ve bunu bir simge olarak görüntüleyin.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// OLE nesneleri eklemek, bu nesneleri saklayan şekiller oluşturur.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Bir şekil bir OLE nesnesi içeriyorsa geçerli bir "OleFormat" özelliğine sahip olacaktır,
// bunu şeklin bazı yönlerini doğrulamak için kullanabiliriz.
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

// Nesne OLE verisi içeriyorsa ona bir akış kullanarak erişebiliriz.
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
