---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words for .NET
description: RtfSaveOptions ExportImagesForOldReaders mülk. Eski okuyucular için anahtar kelimelerin RTFye yazılıp yazılmadığını belirtir. Bu RTF belgesinin boyutunu önemli ölçüde etkileyebilir. Varsayılan değerdoğru  C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

"Eski okuyucular" için anahtar kelimelerin RTF'ye yazılıp yazılmadığını belirtir. Bu, RTF belgesinin boyutunu önemli ölçüde etkileyebilir. Varsayılan değer:`doğru` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Notlar

"Eski okuyucular" Microsoft Word 97 öncesi uygulamalardır ve aynı zamanda WordPad'dir. Bu seçenek seçildiğinde`doğru` Aspose.Words ek RTF anahtar sözcükleri yazar. Bu anahtar sözcükler, belgenin "eski okuyucu" uygulamasında açıldığında doğru şekilde görüntülenmesini sağlar, ancak belgenin boyutunu önemli ölçüde artırabilir.

Bu seçeneği şu şekilde ayarlarsanız`YANLIŞ`, bu durumda "eski okuyucularda" yalnızca WMF, EMF ve BMP formatlarındaki görüntüler görüntülenecektir.

## Örnekler

Özel seçeneklerle bir belgenin .rtf'ye nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi bir RTF'ye kaydetme şeklimizi değiştirmek için belgenin "Kaydet" yöntemine iletilecek bir "RtfSaveOptions" nesnesi oluşturun.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// "ExportCompactSize" özelliğini "true" olarak ayarlayın
// sağdan sola metin uyumluluğu pahasına kaydedilen belgenin boyutunu azaltın.
options.ExportCompactSize = true;

// Belgemizin olduğundan emin olmak amacıyla fazladan anahtar kelimeler kullanmak için "ExportImagesFotOldReaders" özelliğini "true" olarak ayarlayın
// Microsoft Word 97 öncesi okuyucular ve WordPad ile uyumludur.
// Belgenin boyutunu küçültmek için "ExportImagesFotOldReaders" özelliğini "false" olarak ayarlayın,
// ancak eski okuyucuların belgenin içerebileceği meta dosyası olmayan veya BMP görüntülerini okuyabilmesini önleyin.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Ayrıca bakınız

* class [RtfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
