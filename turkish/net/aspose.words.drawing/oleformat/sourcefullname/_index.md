---
title: OleFormat.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words for .NET
description: OleFormat SourceFullName mülk. Bağlantılı OLE nesnesine ilişkin kaynak dosyanın yolunu ve adını alır veya ayarlar C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.drawing/oleformat/sourcefullname/
---
## OleFormat.SourceFullName property

Bağlantılı OLE nesnesine ilişkin kaynak dosyanın yolunu ve adını alır veya ayarlar.

```csharp
public string SourceFullName { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

Eğer`SourceFullName` boş bir dize değil, OLE nesnesi bağlantılı.

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
