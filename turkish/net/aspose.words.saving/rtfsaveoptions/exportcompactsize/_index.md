---
title: RtfSaveOptions.ExportCompactSize
second_title: Aspose.Words for .NET API Referansı
description: RtfSaveOptions mülk. Çıkış RTF belgelerinin boyutunun küçültülmesine izin verir ancak RTL sağdan sola metin içeriyorsa doğru şekilde görüntülenmez. Varsayılan değerYANLIŞ .
type: docs
weight: 20
url: /tr/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Çıkış RTF belgelerinin boyutunun küçültülmesine izin verir, ancak RTL (sağdan sola) metin içeriyorsa doğru şekilde görüntülenmez. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ExportCompactSize { get; set; }
```

### Notlar

Aspose.Words kullanarak RTF'ye dönüştürmek istediğiniz belge Arapça gibi dillerde sağdan sola metni içermiyorsa bu seçeneği şu şekilde ayarlayabilirsiniz:`doğru` Ortaya çıkan RTF'nin boyutunu azaltmak için .

### Örnekler

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
* ad alanı [Aspose.Words.Saving](../../rtfsaveoptions/)
* toplantı [Aspose.Words](../../../)


