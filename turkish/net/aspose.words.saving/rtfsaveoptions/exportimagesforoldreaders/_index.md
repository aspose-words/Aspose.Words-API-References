---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: .NET için Aspose.Words
description: RTF belgelerinizi ExportImagesForOldReaders özelliğiyle optimize edin. Eski okuyucular için anahtar sözcük eklemeyi kontrol edin, dosya boyutunu ve performansı etkileyin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

"Eski okuyucular" için anahtar sözcüklerin RTF'ye yazılıp yazılmadığını belirtir. Bu, RTF belgesinin boyutunu önemli ölçüde etkileyebilir. Varsayılan değer`doğru` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Notlar

"Eski okuyucular" Microsoft Word 97 öncesi uygulamalar ve WordPad'dir. Bu seçenek etkinleştirildiğinde`doğru` Aspose.Words ek RTF anahtar sözcükleri yazar. Bu anahtar sözcükler, belgenin "eski okuyucu" uygulamasında açıldığında doğru şekilde görüntülenmesini sağlar, ancak belgenin boyutunu önemli ölçüde artırabilir.

Bu seçeneği şu şekilde ayarlarsanız`YANLIŞ`o zaman sadece WMF, EMF ve BMP formatlarındaki resimler "eski okuyucularda" gösterilecektir.

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

* class [RtfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
