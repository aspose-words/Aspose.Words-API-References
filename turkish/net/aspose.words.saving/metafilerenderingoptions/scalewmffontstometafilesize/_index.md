---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Aspose.Words for .NET API Referansı
description: MetafileRenderingOptions mülk. WMF meta dosyasındaki yazı tiplerinin sayfadaki meta dosya boyutuna göre ölçeklenip ölçeklendirilmeyeceğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

WMF meta dosyasındaki yazı tiplerinin sayfadaki meta dosya boyutuna göre ölçeklenip ölçeklendirilmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### Notlar

WMF meta dosyaları MS Word'de görüntülendiğinde, yazı tipleri sayfadaki gerçek meta dosyası boyutuna göre ölçeklenebilir.

Bu değer olarak ayarlandığında`doğru`, Aspose.Words, sayfadaki meta dosya boyutuna göre yazı tipi ölçeklendirmesini öykünür.

Bu değer olarak ayarlandığında`yanlış`, Aspose.Words, yazı tiplerini meta dosyası varsayılan boyutuna dönüştürülürken görüntüler.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır.

Varsayılan değer`doğru`.

### Örnekler

Sayfadaki meta dosya boyutuna göre WMF yazı tiplerinin nasıl ölçekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Fontları ölçeklendirmek için "ScaleWmfFontsToMetafileSize" özelliğini "true" olarak ayarlayın
// WMF görüntüleri içindeki metni sayfadaki meta dosyasının boyutuna göre biçimlendiren.
// "ScaleWmfFontsToMetafileSize" özelliğini "false" olarak ayarlayın.
// bu yazı tiplerinin varsayılan ölçeğini koru.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../metafilerenderingoptions/)
* toplantı [Aspose.Words](../../../)


