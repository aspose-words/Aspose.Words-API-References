---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: .NET için Aspose.Words
description: En iyi InkML işleme için Aspose.Words ImlRenderingMode enum'unu keşfedin. Hassas mürekkep nesnesi görselleştirmesiyle belge çıktınızı geliştirin!
type: docs
weight: 6000
url: /tr/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Mürekkep (InkML) nesnelerinin sabit sayfa biçimlerine nasıl işleneceğini belirtir.

```csharp
public enum ImlRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Fallback | `0` | Mürekkep (InkML) nesnesi için geri çekilme şekli mevcutsa, Aspose.Words, InkML yerine geri çekilme şeklini işler. |
| InkML | `1` | Aspose.Words, mürekkep (InkML) nesnesinin geri dönüş şeklini yok sayar ve InkML'nin kendisini işler. Bu varsayılan moddur. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
