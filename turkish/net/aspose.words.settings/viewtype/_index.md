---
title: ViewType Enum
linktitle: ViewType
articleTitle: ViewType
second_title: .NET için Aspose.Words
description: Microsoft Word için Aspose.Words.Settings.ViewType enum'unu keşfedin. Belge sunumunu ve kullanıcı deneyimini geliştirmek için esnek görünüm modlarının kilidini açın.
type: docs
weight: 6790
url: /tr/net/aspose.words.settings/viewtype/
---
## ViewType enumeration

Microsoft Word'deki görüntüleme modu için olası değerler.

```csharp
public enum ViewType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Belge, uygulamanın varsayılan görünümünde işlenecektir. |
| Reading | `0` | Belge, uygulamanın varsayılan görünümünde işlenecektir. |
| PageLayout | `1` | Belge, yazdırılacağı şekliyle görüntüleyen bir görünümde açılacaktır. |
| Outline | `3` | Belge, uzun belgelerin ana hatlarını çıkarmak veya oluşturmak için optimize edilmiş bir görünümde işlenmelidir. |
| Normal | `4` | Belge, uzun belgelerin ana hatlarını çıkarmak veya oluşturmak için optimize edilmiş bir görünümde işlenmelidir. |
| Web | `5` | Belge, bu belgenin bir web sayfasında görüntüleneceği şekilde taklit edilen bir görünümde işlenecektir. |

## Örnekler

Microsoft Word'ün eski sürümlerinin bir belgeyi yüklerken uygulayacağı özel yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### Ayrıca bakınız

* class [ViewOptions](../viewoptions/)
* property [ViewType](../viewoptions/viewtype/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
