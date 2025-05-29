---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: .NET için Aspose.Words
description: Gelişmiş belge kalitesi ve görsel çekicilik için renk oluşturmayı özelleştirmek üzere FixedPageSaveOptions ColorMode özelliğini keşfedin. Çıktınızı bugün optimize edin!
type: docs
weight: 10
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Renklerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public ColorMode ColorMode { get; set; }
```

## Notlar

Varsayılan değer:Normal .

## Örnekler

Resim renginin kaydetme seçenekleri özelliği ile nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
// Belgedeki tüm görselleri siyah beyaz yapmak için "ColorMode" özelliğini "Gri Tonlamalı" olarak ayarlayın.
// Bu ayarla çıktı belgesinin boyutu daha büyük olabilir.
// Tüm görselleri renkli hale getirmek için "ColorMode" özelliğini "Normal" olarak ayarlayın.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
