---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: .NET için Aspose.Words
description: Gelişmiş üretkenlik ve kişiselleştirilmiş düzenleme deneyimi için Microsoft Word görünüm modunuzu kolayca özelleştirmek üzere ViewOptions ViewType özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Microsoft Word'deki görünüm modunu kontrol eder.

```csharp
public ViewType ViewType { get; set; }
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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
