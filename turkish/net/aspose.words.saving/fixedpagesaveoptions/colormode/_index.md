---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words for .NET
description: FixedPageSaveOptions ColorMode mülk. Renklerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Renklerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar.

```csharp
public ColorMode ColorMode { get; set; }
```

## Notlar

Varsayılan değer:Normal .

## Örnekler

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

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
