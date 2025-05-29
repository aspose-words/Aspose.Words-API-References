---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Belgelerinizi RTF formatında zahmetsizce kaydetmek, uyumluluğu ve kolay paylaşımı garantilemek için RtfSaveOptions SaveFormat özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

Bir belgenin özel seçeneklerle .rtf formatına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgenin "Kaydet" yöntemine, belgeyi RTF'ye nasıl kaydedeceğimizi değiştirmek için geçirilecek bir "RtfSaveOptions" nesnesi oluşturun.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// "ExportCompactSize" özelliğini "true" olarak ayarlayın
// Sağdan sola metin uyumluluğu pahasına kaydedilen belgenin boyutunu küçült.
options.ExportCompactSize = true;

// Belgemizin doğru olduğundan emin olmak için ek anahtar sözcükler kullanmak üzere "ExportImagesFotOldReaders" özelliğini "true" olarak ayarlayın.
// Microsoft Word 97 öncesi okuyucular ve WordPad ile uyumludur.
// Belgenin boyutunu küçültmek için "ExportImagesFotOldReaders" özelliğini "false" olarak ayarlayın,
// ancak eski okuyucuların belgenin içerebileceği meta dosyası veya BMP dışındaki görüntüleri okumasını engeller.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
