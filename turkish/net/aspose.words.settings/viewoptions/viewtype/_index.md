---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words for .NET
description: ViewOptions ViewType mülk. Microsoft Worddeki görüntüleme modunu kontrol eder C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Microsoft Word'deki görüntüleme modunu kontrol eder.

```csharp
public ViewType ViewType { get; set; }
```

## Notlar

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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
