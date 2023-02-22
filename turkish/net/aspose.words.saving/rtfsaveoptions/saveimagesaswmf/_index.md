---
title: RtfSaveOptions.SaveImagesAsWmf
second_title: Aspose.Words for .NET API Referansı
description: RtfSaveOptions mülk. Doğru olduğunda tüm resimler WMF olarak kaydedilecektir.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

Doğru olduğunda, tüm resimler WMF olarak kaydedilecektir.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

### Notlar

Bu seçenek, WordPad uyarı mesajlarından kaçınmanıza yardımcı olabilir.

### Örnekler

Belgeyi RTF olarak kaydederken bir belgedeki tüm görüntülerin nasıl Windows Meta Dosyası biçimine dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.AreEqual(ImageType.Jpeg, imageShape.ImageData.ImageType);

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ImageType.Png, imageShape.ImageData.ImageType);

// Bir RTF'ye kaydetme şeklimizi değiştirmek için belgenin "Kaydet" yöntemine geçmek için bir "RtfSaveOptions" nesnesi oluşturun.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Belgedeki tüm görüntüleri RTF'ye kaydederken WMF'ye dönüştürmek için "SaveImagesAsWmf" özelliğini "true" olarak ayarlayın.
// Bunu yapmak, WordPad gibi okuyucuların belgemizi okumasına yardımcı olacaktır.
// Belgedeki tüm görüntülerin orijinal biçimini korumak için "SaveImagesAsWmf" özelliğini "false" olarak ayarlayın
// RTF'ye kaydettiğimiz gibi. Bu, eski RTF okuyucularıyla uyumluluk pahasına görüntülerin kalitesini koruyacaktır.
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[1]).ImageData.ImageType);
}
else
{
    Assert.AreEqual(ImageType.Jpeg, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Png, ((Shape)shapes[1]).ImageData.ImageType);
}
```

### Ayrıca bakınız

* class [RtfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../rtfsaveoptions/)
* toplantı [Aspose.Words](../../../)


