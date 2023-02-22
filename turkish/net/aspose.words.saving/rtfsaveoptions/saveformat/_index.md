---
title: RtfSaveOptions.SaveFormat
second_title: Aspose.Words for .NET API Referansı
description: RtfSaveOptions mülk. Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaRtf .
type: docs
weight: 40
url: /tr/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Örnekler

Özel seçeneklerle bir belgenin .rtf'ye nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir RTF'ye kaydetme şeklimizi değiştirmek için belgenin "Kaydet" yöntemine geçmek için bir "RtfSaveOptions" nesnesi oluşturun.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// "ExportCompactSize" özelliğini "true" olarak ayarlayın
// sağdan sola metin uyumluluğu pahasına kaydedilen belgenin boyutunu küçültün.
options.ExportCompactSize = true;

// Belgemizin doğru olduğundan emin olmak için fazladan anahtar kelimeler kullanmak için "ExportImagesFotOldReaders" özelliğini "true" olarak ayarlayın.
// Microsoft Word 97 öncesi okuyucular ve WordPad ile uyumludur.
// Belgenin boyutunu küçültmek için "ExportImagesFotOldReaders" özelliğini "false" olarak ayarlayın,
// ancak eski okuyucuların belgenin içerebileceği meta dosyası olmayan veya BMP görüntülerini okumasını önleyin.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../rtfsaveoptions/)
* toplantı [Aspose.Words](../../../)


