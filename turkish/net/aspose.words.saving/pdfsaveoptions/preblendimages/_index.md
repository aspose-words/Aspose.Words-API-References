---
title: PdfSaveOptions.PreblendImages
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Saydam görüntülerin siyah arka plan rengiyle önceden karıştırılıp karıştırılmayacağını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 230
url: /tr/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Saydam görüntülerin siyah arka plan rengiyle önceden karıştırılıp karıştırılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool PreblendImages { get; set; }
```

### Notlar

Görüntülerin önceden karıştırılması, Adobe Reader'da PDF belgesinin görsel görünümünü iyileştirebilir ve kenar yumuşatma yapılarını kaldırabilir.

Önceden harmanlanmış görüntüleri düzgün bir şekilde görüntülemek için, PDF görüntüleyici uygulamasının yumuşak maskeli görüntü sözlüğünde /Mat girişini desteklemesi gerekir. Ayrıca önceden karıştırılmış görüntüler PDF oluşturma performansını düşürebilir.

Varsayılan değer`yanlış`.

### Örnekler

Bir belgeyi PDF'ye kaydederken saydam arka plana sahip görüntülerin nasıl önceden karıştırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Saydam görüntüleri önceden karıştırmak için "PreblendImages" özelliğini "true" olarak ayarlayın
// artefaktları azaltabilecek bir arka plana sahip.
// Saydam görüntüleri normal şekilde oluşturmak için "PreblendImages" özelliğini "false" olarak ayarlayın.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Saydam arka planlara sahip görüntülerin nasıl önceden karıştırılacağını gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Saydam görüntüleri önceden karıştırmak için "PreblendImages" özelliğini "true" olarak ayarlayın
// artefaktları azaltabilecek bir arka plana sahip.
// Saydam görüntüleri normal şekilde oluşturmak için "PreblendImages" özelliğini "false" olarak ayarlayın.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


