---
title: Enum ImlRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.ImlRenderingMode Sıralama. Mürekkep InkML nesnelerinin sabit sayfa formatlarına nasıl aktarılacağını belirtir.
type: docs
weight: 5250
url: /tr/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Mürekkep (InkML) nesnelerinin sabit sayfa formatlarına nasıl aktarılacağını belirtir.

```csharp
public enum ImlRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Fallback | `0` | Mürekkep (InkML) nesnesi için geri dönüş şekli mevcutsa Aspose.Words, InkML yerine geri dönüş şeklini oluşturur. |
| InkML | `1` | Aspose.Words, mürekkep (InkML) nesnesinin geri dönüş şeklini yok sayar ve InkML'nin kendisini oluşturur. Bu, varsayılan moddur. |

### Örnekler

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


