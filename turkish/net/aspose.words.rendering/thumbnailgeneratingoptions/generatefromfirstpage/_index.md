---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: .NET için Aspose.Words
description: GenerateFromFirstPage seçeneğinin belgenin ilk sayfasından veya görüntüsünden küçük resimler oluşturarak görsel içeriğinizi zahmetsizce nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Küçük resmin belgenin ilk sayfasından mı yoksa ilk görüntüden mi oluşturulacağını belirtir.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## Notlar

Varsayılan`doğru` , bu da küçük resmin belgenin ilk sayfasından oluşturulacağı anlamına gelir. Değer ise`YANLIŞ` ve belgede resim yoksa, küçük resim belgenin ilk sayfasından oluşturulacaktır.

## Örnekler

Bir belgenin küçük resminin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Bir belgeyi .epub olarak kaydederken küçük resim görüntüsünü ayarlamanın iki yolu vardır.
// 1 - Belgenin ilk sayfasını kullan:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Belgede bulunan ilk resmi kullan:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Ayrıca bakınız

* class [ThumbnailGeneratingOptions](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
