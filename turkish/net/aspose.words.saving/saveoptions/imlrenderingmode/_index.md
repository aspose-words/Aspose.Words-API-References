---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: .NET için Aspose.Words
description: SaveOptions ImlRenderingMode özelliğinin InkML nesne işlemeyi nasıl geliştirdiğini keşfedin. Daha iyi görsel sonuçlar için mürekkep işlemenizi optimize edin!
type: docs
weight: 90
url: /tr/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Mürekkep (InkML) nesnelerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Notlar

Varsayılan değer:InkML .

Bu özellik, belge sabit sayfa biçimlerine aktarıldığında kullanılır.

## Örnekler

Ink nesnesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// 'ImlRenderingMode.InkML' ayarı, mürekkep (InkML) nesnesinin geri dönüş şeklini yok sayar ve InkML'nin kendisini işler.
// Eğer render sonucu tatmin edici değilse,
// Önceki versiyonlara benzer bir sonuç almak için lütfen 'ImlRenderingMode.Fallback' kullanın.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Ayrıca bakınız

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
