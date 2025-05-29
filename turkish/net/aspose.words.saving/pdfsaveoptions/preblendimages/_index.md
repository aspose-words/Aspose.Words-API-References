---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: .NET için Aspose.Words
description: PdfSaveOptions' PreblendImages özelliğini keşfedin. Gelişmiş belge kalitesi ve görsel çekicilik için şeffaf görüntü harmanlamayı kolayca kontrol edin.
type: docs
weight: 270
url: /tr/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Şeffaf resimlerin siyah arka plan rengiyle önceden karıştırılıp karıştırılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool PreblendImages { get; set; }
```

## Notlar

Görüntülerin önceden karıştırılması, Adobe Reader'da PDF belgelerinin görsel görünümünü iyileştirebilir ve kenar yumuşatma bozukluklarını giderebilir.

Önceden karıştırılmış görüntüleri düzgün bir şekilde görüntülemek için PDF görüntüleyici uygulamasının yumuşak maskeli görüntü sözlüğünde /Matte girişini desteklemesi gerekir. Ayrıca görüntüleri önceden karıştırmak PDF oluşturma performansını düşürebilir.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Bir belgeyi PDF'e kaydederken şeffaf arka plana sahip görsellerin önceden nasıl karıştırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();
// Şeffaf görüntüleri önceden karıştırmak için "PreblendImages" özelliğini "true" olarak ayarlayın
// eserleri azaltabilecek bir arka planla.
// Şeffaf görüntüleri normal şekilde oluşturmak için "PreblendImages" özelliğini "false" olarak ayarlayın.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
