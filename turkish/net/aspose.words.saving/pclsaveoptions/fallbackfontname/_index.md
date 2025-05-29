---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: .NET için Aspose.Words
description: İstediğiniz yazı tipi mevcut olmadığında varsayılan yazı tipiyle sorunsuz bir şekilde yazdırmayı sağlayan PclSaveOptions FallbackFontName özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Yazıcıda ve yerleşik yazı tipleri koleksiyonlarında beklenen yazı tipi bulunamazsa kullanılacak yazı tipinin adı.

```csharp
public string FallbackFontName { get; set; }
```

## Notlar

Eğer bir geri dönüş bulunamazsa, bir uyarı üretilir ve "Arial" yazı tipi kullanılır.

## Örnekler

Yazıcının orijinal yazı tipinin kullanılamaması durumunda, basılı metne yedek olarak uygulayacağı yazı tipinin nasıl bildirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Bu belge, yazıcıya eksik yazı tipine sahip metne "Times New Roman" uygulamasını söyleyecektir.
// "Times New Roman" da mevcut değilse yazıcı varsayılan olarak "Arial" yazı tipini kullanacaktır.
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Ayrıca bakınız

* class [PclSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
