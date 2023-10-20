---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words for .NET
description: ViewOptions ZoomPercent mülk. Belgenizi görüntülemek istediğiniz yüzdeyi 10 ile 500 arasında alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Belgenizi görüntülemek istediğiniz yüzdeyi (10 ile 500 arasında) alır veya ayarlar.

```csharp
public int ZoomPercent { get; set; }
```

## Notlar

Değer 0 ise bu özellik bunun yerine 100'ü kullanır, aksi takdirde değer 10'dan küçük veya 500'den büyükse bu özellik atar.

Aspose.Words bu seçeneği okuyup yazabilse de kullanımı uygulamaya özeldir. Örneğin MS Word 2013 bu seçeneğin değerini dikkate almaz.

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

* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
