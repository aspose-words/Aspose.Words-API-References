---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words for .NET
description: SaveOptions ImlRenderingMode mülk. Mürekkep InkML nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Mürekkep (InkML) nesnelerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Notlar

Varsayılan değer:InkML .

Bu özellik, belge sabit sayfa formatlarına aktarıldığında kullanılır.

## Örnekler

Mürekkep nesnesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// 'ImlRenderingMode.InkML'yi ayarla, mürekkep (InkML) nesnesinin geri dönüş şeklini yok sayar ve InkML'nin kendisini oluşturur.
// Eğer render sonucu tatmin edici değilse,
// önceki sürümlere benzer bir sonuç elde etmek için lütfen 'ImlRenderingMode.Fallback'i kullanın.
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
