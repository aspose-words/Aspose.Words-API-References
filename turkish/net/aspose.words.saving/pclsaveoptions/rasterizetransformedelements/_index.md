---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: .NET için Aspose.Words
description: PCL belgelerindeki karmaşık öğelerin rasterleştirilmesini PclSaveOptions ile kontrol edin. En iyi sonuçlar için görüntü kalitesini ve dosya boyutunu kolayca yönetin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Karmaşık dönüştürülmüş elements 'nin PCL belgesine kaydedilmeden önce rasterleştirilip rasterleştirilmeyeceğini belirleyen bir değer alır veya ayarlar. Varsayılan`doğru` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Notlar

PCL, Aspose Words tarafından kullanılan bazı dönüşümleri desteklemez. Örn. döndürülmüş, eğik resimler ve doku fırçaları. Bu tür öğeleri düzgün bir şekilde işlemek için rasterleştirme işlemi kullanılır, yani resme kaydetme ve kırpma. Bu işlem ek zaman ve bellek alabilir. Eğer bayrak`YANLIŞ` , çıktıdaki bazı içerikler kaynak belgeyle karşılaştırıldığında farklı olabilir.

## Örnekler

Bir belgeyi PCL'ye kaydederken karmaşık öğelerin nasıl rasterleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Ayrıca bakınız

* class [PclSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
