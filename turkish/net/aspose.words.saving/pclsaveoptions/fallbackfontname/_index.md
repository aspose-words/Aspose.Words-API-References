---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words for .NET
description: PclSaveOptions FallbackFontName mülk. Yazıcıda ve yerleşik yazı tipi koleksiyonlarında beklenen yazı tipi bulunamazsa kullanılacak yazı tipinin adı  C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Yazıcıda ve yerleşik yazı tipi koleksiyonlarında beklenen yazı tipi bulunamazsa kullanılacak yazı tipinin adı .

```csharp
public string FallbackFontName { get; set; }
```

## Notlar

Geri dönüş bulunamazsa uyarı oluşturulur ve "Arial" yazı tipi kullanılır.

## Örnekler

Orijinal yazı tipinin mevcut olmaması durumunda, yazıcının basılı metne yedek olarak uygulayacağı yazı tipinin nasıl bildirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Bu belge, yazıcıya eksik yazı tipine sahip metne "Times New Roman" uygulaması talimatını verecektir.
// "Times New Roman" da mevcut değilse, yazıcı varsayılan olarak "Arial" yazı tipini kullanır.
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Ayrıca bakınız

* class [PclSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
