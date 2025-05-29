---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: .NET için Aspose.Words
description: Optimize edilmiş renk oluşturma için Aspose.Words.Saving.ColorMode enum'unu keşfedin. Hassas renk ayarlarıyla belgenizin görsel çekiciliğini artırın.
type: docs
weight: 5600
url: /tr/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Renklerin nasıl işleneceğini belirtir.

```csharp
public enum ColorMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Değiştirilmemiş renklerle oluşturma. |
| Grayscale | `1` | Beyazdan siyaha kadar çeşitli gri tonlarında renklerle render alma. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
