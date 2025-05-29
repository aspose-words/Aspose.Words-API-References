---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: .NET için Aspose.Words
description: ExportCompactSize özelliğiyle RTF belge boyutunu optimize edin. RTL içerikle bile metin bütünlüğünü korurken verimli depolama sağlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Çıktı RTF belgelerinin boyutunu küçültmeye izin verir, ancak RTL (sağdan sola) metin içeriyorlarsa doğru şekilde görüntülenmezler. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Notlar

Aspose.Words kullanarak RTF'ye dönüştürmek istediğiniz belge Arapça gibi dillerde sağdan sola metin içermiyorsa, bu seçeneği şu şekilde ayarlayabilirsiniz:`doğru` Ortaya çıkan RTF'nin boyutunu küçültmek için .

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
