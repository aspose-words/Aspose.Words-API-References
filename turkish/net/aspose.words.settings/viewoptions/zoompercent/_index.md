---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: .NET için Aspose.Words
description: Belgenizin yakınlaştırma seviyesini %10-500 arasında ayarlamak için ViewOptions ZoomPercent özelliğini ayarlayın. Okunabilirliği artırın ve görüntüleme deneyiminizi optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Belgenizi görüntülemek istediğiniz yüzdeyi alır veya ayarlar.

```csharp
public int ZoomPercent { get; set; }
```

## Notlar

Aspose.Words bu seçeneği okuyup yazabilmesine rağmen, kullanımı uygulamaya özgüdür. Örneğin MS Word 2013 bu seçeneğin değerine saygı göstermez.

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

* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
