---
title: PdfSaveOptions.CacheBackgroundGraphics
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Belgenin arka planına yerleştirilen grafiklerin önbelleğe alınıp alınmayacağını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Belgenin arka planına yerleştirilen grafiklerin önbelleğe alınıp alınmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

### Notlar

Varsayılan değer:`doğru` ve arka plan grafikleri PDF belgesine xObject olarak yazılır.

Değer ne zaman`YANLIŞ` arka plan grafikleri önbelleğe alınmaz.

Bazı şekiller önbelleğe alma için desteklenmez (alanlar, yer imleri, HRef'ler içeren şekiller).

Belge arka plan grafiği, bir sayfanın arka planı ve kenarlığının yanı sıra altbilgiye veya üstbilgiye yerleştirilen çeşitli şekiller, grafikler, resimlerdir.

### Örnekler

Belgenin arka planına yerleştirilen grafiklerin nasıl önbelleğe alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


