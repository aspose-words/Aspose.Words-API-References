---
title: ViewOptions.ZoomType
linktitle: ZoomType
articleTitle: ZoomType
second_title: .NET için Aspose.Words
description: Kullanıcı deneyimini ve arayüz esnekliğini geliştirmek için pencere boyutuna göre yakınlaştırma düzeylerini kolayca ayarlamak üzere ViewOptions ZoomType özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

Pencerenin boyutuna göre bir yakınlaştırma değeri alır veya ayarlar.

```csharp
public ZoomType ZoomType { get; set; }
```

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

Microsoft Word'ün eski sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma türünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.PageWidth" olarak ayarlayın
// belgeyi sayfanın genişliğine uyacak şekilde otomatik olarak yakınlaştırmak için.
// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.FullPage" olarak ayarlayın
// Belgenin ilk sayfasının tamamını görünür hale getirmek için otomatik olarak yakınlaştırma yapmak.
// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.TextFit" olarak ayarlayın
// Belgeyi ilk sayfanın iç metin kenar boşluklarına uyacak şekilde otomatik olarak yakınlaştırmak için.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Ayrıca bakınız

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
