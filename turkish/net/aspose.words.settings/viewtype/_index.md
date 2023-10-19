---
title: ViewType Enum
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.ViewType Sıralama. Microsoft Worddeki görüntüleme modu için olası değerler C#'da.
type: docs
weight: 5960
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
| None | `0` | Belge, uygulamanın varsayılan görünümünde oluşturulacaktır. |
| Reading | `0` | Belge, uygulamanın varsayılan görünümünde oluşturulacaktır. |
| PageLayout | `1` | Belge, belgeyi yazdırılacağı şekliyle görüntüleyen bir görünümde açılacaktır. |
| Outline | `3` | Belge, uzun belgelerin ana hatlarını çizmek veya oluşturmak için optimize edilmiş bir görünümde oluşturulacaktır. |
| Normal | `4` | Belge, uzun belgelerin ana hatlarını çizmek veya oluşturmak için optimize edilmiş bir görünümde oluşturulacaktır. |
| Web | `5` | Belge, bu belgenin bir web sayfasında görüntülenme şeklini taklit eden bir görünümde oluşturulacaktır. |

## Örnekler

Microsoft Word'ün eski sürümlerinin yükleme sırasında bir belgeye uygulayacağı özel yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

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
