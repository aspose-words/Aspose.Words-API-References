---
title: PclSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Projelerinizde uyumluluğu ve yüksek kaliteli çıktıyı garanti altına almak için PclSaveOptions SaveFormat özelliğini kullanarak belgeleri PCL formatında kolayca kaydedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaPcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
