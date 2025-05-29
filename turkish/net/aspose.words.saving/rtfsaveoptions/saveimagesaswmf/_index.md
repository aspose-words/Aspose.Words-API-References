---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: .NET için Aspose.Words
description: RtfSaveOptions SaveImagesAsWmf özelliğinin, tüm görüntüleri üstün kalite ve uyumluluk için WMF olarak kaydederek belgenizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

Ne zaman`doğru` tüm resimler WMF. olarak kaydedilecek

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## Notlar

Bu seçenek WordPad uyarı mesajlarından kaçınmaya yardımcı olabilir.

## Örnekler

Belgeyi RTF olarak kaydettiğimizde, belgedeki tüm görsellerin Windows Metafile formatına nasıl dönüştürüleceğini gösterir.

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

// Belgenin "Kaydet" yöntemine, belgeyi RTF'ye nasıl kaydedeceğimizi değiştirmek için geçirilecek bir "RtfSaveOptions" nesnesi oluşturun.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Belgeyi RTF olarak kaydettiğimizde içindeki tüm görselleri WMF'ye dönüştürmek için "SaveImagesAsWmf" özelliğini "true" olarak ayarlayın.
// Bunu yapmak WordPad gibi okuyucuların belgemizi okumasına yardımcı olacaktır.
// Belgedeki tüm resimlerin orijinal biçimini korumak için "SaveImagesAsWmf" özelliğini "false" olarak ayarlayın
// RTF'ye kaydettiğimizde. Bu, eski RTF okuyucularıyla uyumluluk pahasına görüntülerin kalitesini koruyacaktır.
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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
