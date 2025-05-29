---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: .NET için Aspose.Words
description: MergeToImages yöntemi ile birden fazla belgeyi zahmetsizce birleştirerek, dosya adlarını ve kaydetme seçeneklerini özelleştirerek tek bir görüntü çıktısı oluşturun.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

Belirtilen giriş-çıkış dosya adlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. Çıktıyı resimlere dönüştürür.

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFiles | String[] | Giriş dosya adları. |
| saveOptions | ImageSaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

Belirtilen görüntü kaydetme seçeneklerini kullanarak verilen giriş belge akışlarını tek bir çıktı belgesinde birleştirir. Çıktıyı görüntülere dönüştürür.

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStreams | Stream[] | Giriş dosyası akışları. |
| saveOptions | ImageSaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
