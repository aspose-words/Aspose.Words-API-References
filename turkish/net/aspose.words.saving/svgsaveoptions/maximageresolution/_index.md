---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: .NET için Aspose.Words
description: SvgSaveOptions MaxImageResolution ile dışa aktardığınız raster görüntülerinizin kalitesini kontrol edin. En iyi sonuçlar için piksel yoğunluğunu ayarlayın. Varsayılan, 0.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Dışa aktarılan raster görüntülerin çözünürlüğünü sınırlayan inç başına piksel cinsinden bir değer alır veya ayarlar. Varsayılan değer sıfırdır.

```csharp
public int MaxImageResolution { get; set; }
```

## Notlar

Bu özelliğin değeri sıfırdan farklıysa, dışa aktarılan raster görüntülerin çözünürlüğünü sınırlar. Yani, daha yüksek çözünürlüklü görüntüler sınıra kadar yeniden örneklenir ve daha düşük çözünürlüklü görüntüler olduğu gibi dışa aktarılır.

Bu özelliğin değeri sıfırsa, tüm raster görüntüleri yeniden örnekleme yapılmadan dışa aktarılır.

## Örnekler

Görüntü çözünürlüğü için sınır belirlemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### Ayrıca bakınız

* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
