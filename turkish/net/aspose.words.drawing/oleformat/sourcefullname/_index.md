---
title: OleFormat.SourceFullName
second_title: Aspose.Words for .NET API Referansı
description: OleFormat mülk. Bağlantılı OLE nesnesi için kaynak dosyanın yolunu ve adını alır veya ayarlar.
type: docs
weight: 100
url: /tr/net/aspose.words.drawing/oleformat/sourcefullname/
---
## OleFormat.SourceFullName property

Bağlantılı OLE nesnesi için kaynak dosyanın yolunu ve adını alır veya ayarlar.

```csharp
public string SourceFullName { get; set; }
```

### Notlar

Varsayılan değer boş bir dizedir.

Eğer`SourceFullName` boş bir dize değilse, OLE nesnesi bağlantılıdır.

### Örnekler

Bağlı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Microsoft Visio çizimini belgeye OLE nesnesi olarak gömün.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Yerel dosya sisteminde dosyaya bir bağlantı ekleyin ve onu bir simge olarak görüntüleyin.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// OLE nesnelerinin eklenmesi, bu nesneleri depolayan şekiller oluşturur.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Bir şekil bir OLE nesnesi içeriyorsa, geçerli bir "OleFormat" özelliğine sahip olacaktır,
// şeklin bazı yönlerini doğrulamak için kullanabileceğimiz.
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

// Nesne OLE verisi içeriyorsa, ona bir akış kullanarak erişebiliriz.
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


