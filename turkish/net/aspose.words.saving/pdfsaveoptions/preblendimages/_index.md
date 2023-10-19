---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words for .NET
description: PdfSaveOptions PreblendImages mülk. Saydam görüntülerin siyah arka plan rengiyle önceden karıştırılıp karıştırılmayacağını belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 260
url: /tr/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Saydam görüntülerin siyah arka plan rengiyle önceden karıştırılıp karıştırılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool PreblendImages { get; set; }
```

## Notlar

Görüntülerin önceden harmanlanması, Adobe Reader'da PDF belgesinin görsel görünümünü iyileştirebilir ve kenar yumuşatma bozulmalarını ortadan kaldırabilir.

Önceden harmanlanmış görüntüleri düzgün bir şekilde görüntülemek için, PDF görüntüleyici uygulamasının yumuşak maskeli görüntü sözlüğünde /Matte girişini desteklemesi gerekir. Ayrıca görüntülerin önceden harmanlanması PDF oluşturma performansını düşürebilir.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Bir belgeyi PDF'ye kaydederken şeffaf arka planlı görüntülerin nasıl önceden karıştırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Şeffaf görüntüleri önceden karıştırmak için "PreblendImages" özelliğini "true" olarak ayarlayın
// artefaktları azaltabilecek bir arka plan ile.
// Şeffaf görüntüleri normal şekilde işlemek için "PreblendImages" özelliğini "false" olarak ayarlayın.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Şeffaf arka planlara sahip görsellerin nasıl önceden karıştırılacağını gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Şeffaf görüntüleri önceden karıştırmak için "PreblendImages" özelliğini "true" olarak ayarlayın
// artefaktları azaltabilecek bir arka plan ile.
// Şeffaf görüntüleri normal şekilde işlemek için "PreblendImages" özelliğini "false" olarak ayarlayın.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
