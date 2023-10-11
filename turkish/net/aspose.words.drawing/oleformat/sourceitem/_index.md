---
title: OleFormat.SourceItem
second_title: Aspose.Words for .NET API Referansı
description: OleFormat mülk. Kaynak dosyanın bağlanan kısmını tanımlamak için kullanılan bir dizeyi alır veya ayarlar.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/oleformat/sourceitem/
---
## OleFormat.SourceItem property

Kaynak dosyanın bağlanan kısmını tanımlamak için kullanılan bir dizeyi alır veya ayarlar.

```csharp
public string SourceItem { get; set; }
```

### Notlar

Varsayılan değer boş bir dizedir.

Örneğin, kaynak dosya bir Microsoft Excel çalışma kitabıysa,`SourceItem` OLE nesnesi çalışma sayfasından yalnızca birkaç hücre içeriyorsa, özelliği "Çalışma Kitabı1!R3C1:R4C2" değerini döndürebilir.

### Örnekler

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
* ad alanı [Aspose.Words.Drawing](../../oleformat/)
* toplantı [Aspose.Words](../../../)


