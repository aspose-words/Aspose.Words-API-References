---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: .NET için Aspose.Words
description: MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution özelliğini keşfedin. En iyi sayfa görüntülemesi için metafile işleme çözünürlüğünü kontrol edin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Sayfadaki boyuta meta dosya oluşturma emülasyonu için piksel/inç cinsinden çözünürlüğü alır veya ayarlar.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Notlar

Bu seçenek yalnızca şu durumlarda kullanılır:[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) ayarlandı`doğru`.

Varsayılan değer 96'dır. Bu varsayılan bir görüntüleme çözünürlüğüdür. Yani meta dosyası oluşturma, meta dosyasının MS Word'deki görüntüsünü %100 yakınlaştırma faktörüyle taklit edecektir.

## Örnekler

Sayfadaki boyuta göre meta dosyasının nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmulateRenderingToSizeOnPage" özelliğini "true" olarak ayarlayın
// Sayfadaki meta dosya boyutuna göre işlemeyi taklit etmek için.
// "EmulateRenderingToSizeOnPage" özelliğini "false" olarak ayarlayın
// meta dosyası oluşturmayı varsayılan piksel boyutuna benzetmek için.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
