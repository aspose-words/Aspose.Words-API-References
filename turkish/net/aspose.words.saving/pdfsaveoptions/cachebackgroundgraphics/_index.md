---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: .NET için Aspose.Words
description: Belge grafik önbelleğini optimize etmek, PDF oluşturma ve performansınızı artırmak için PdfSaveOptions CacheBackgroundGraphics özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Belgenin arka planına yerleştirilen grafiklerin önbelleğe alınıp alınmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Notlar

Varsayılan değer`doğru` ve arka plan grafikleri xObject olarak PDF belgesine yazılır.

Değer ne zaman`YANLIŞ` arka plan grafikleri önbelleğe alınmaz.

Bazı şekiller önbelleğe alma için desteklenmez (alanlı şekiller, yer imleri, HRef'ler).

Belge arka plan grafiği, sayfanın alt bilgisine veya üst bilgisine yerleştirilen çeşitli şekiller, grafikler, resimler ve arka plan ile kenarlıklardan oluşur.

## Örnekler

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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
