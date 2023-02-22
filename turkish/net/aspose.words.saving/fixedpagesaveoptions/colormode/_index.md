---
title: FixedPageSaveOptions.ColorMode
second_title: Aspose.Words for .NET API Referansı
description: FixedPageSaveOptions mülk. Renklerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Renklerin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar.

```csharp
public ColorMode ColorMode { get; set; }
```

### Notlar

Varsayılan değerNormal .

### Örnekler

Seçenekleri kaydetme özelliği ile görüntü renginin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
// Belgedeki tüm görüntüleri siyah beyaz işlemek için "ColorMode" özelliğini "Gri Tonlamalı" olarak ayarlayın.
// Çıktı belgesinin boyutu bu ayarla daha büyük olabilir.
// Tüm görüntüleri renkli hale getirmek için "ColorMode" özelliğini "Normal" olarak ayarlayın.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* toplantı [Aspose.Words](../../../)


