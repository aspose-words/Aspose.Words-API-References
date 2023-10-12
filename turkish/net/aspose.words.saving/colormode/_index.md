---
title: Enum ColorMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.ColorMode Sıralama. Renklerin nasıl oluşturulacağını belirtir.
type: docs
weight: 4860
url: /tr/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Renklerin nasıl oluşturulacağını belirtir.

```csharp
public enum ColorMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Değiştirilmemiş renklerle görüntü oluşturma. |
| Grayscale | `1` | Beyazdan siyaha kadar çeşitli gri tonlarındaki renklerle görüntü oluşturma. |

### Örnekler

Kaydetme seçenekleri özelliğiyle görüntü renginin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
// Belgedeki tüm görüntüleri siyah beyaz oluşturmak için "ColorMode" özelliğini "Gri Tonlamalı" olarak ayarlayın.
// Bu ayarla çıktı belgesinin boyutu daha büyük olabilir.
// Tüm görüntüleri renkli oluşturmak için "ColorMode" özelliğini "Normal" olarak ayarlayın.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


