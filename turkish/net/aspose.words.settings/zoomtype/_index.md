---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: .NET için Aspose.Words
description: Microsoft Word'de en iyi görüntüleme ve üretkenlik için belge görüntüleme boyutlarını özelleştirmek üzere Aspose.Words.Settings.ZoomType enum'unu keşfedin.
type: docs
weight: 6810
url: /tr/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Microsoft Word'de belgenin ekranda ne kadar büyük veya küçük görüneceğine ilişkin olası değerler.

```csharp
public enum ZoomType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Custom | `0` | Yakınlaştırma yüzdesi açıkça ayarlanır. Kontrol boyutu değiştiğinde otomatik olarak yeniden hesaplanmaz. |
| None | `0` | Açık yakınlaştırma yüzdesini kullanmayı belirtir. AynıCustom . |
| FullPage | `1` | Yakınlaştırma yüzdesi, tam bir sayfaya sığacak şekilde otomatik olarak yeniden hesaplanır. |
| PageWidth | `2` | Yakınlaştırma yüzdesi sayfa genişliğine uyacak şekilde otomatik olarak yeniden hesaplanır. |
| TextFit | `3` | Yakınlaştırma yüzdesi metne uyacak şekilde otomatik olarak yeniden hesaplanır. |

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
* property [ZoomType](../viewoptions/zoomtype/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
