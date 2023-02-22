---
title: Class ViewOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.ViewOptions sınıf. Bir belgenin Microsoft Wordde nasıl gösterileceğini kontrol eden çeşitli seçenekler sunar.
type: docs
weight: 5650
url: /tr/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Bir belgenin Microsoft Word'de nasıl gösterileceğini kontrol eden çeşitli seçenekler sunar.

```csharp
public class ViewOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Baskı düzeni görünümünde arka plan şeklinin görüntüsünü kontrol eder. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Belgenin form tasarım modunda olup olmadığını belirtir. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Microsoft Word'de görüntüleme modunu kontrol eder. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Belgenizi görüntülemek istediğiniz yüzdeyi (10 ile 500 arasında) alır veya ayarlar. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Pencerenin boyutuna göre bir yakınlaştırma değeri alır veya ayarlar. |

### Örnekler

Microsoft Word'ün eski sürümlerinin yükleme sırasında bir belgeye uygulanacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

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

Microsoft Word'ün eski sürümlerinin yükleme sırasında bir belgeye uygulanacağı özel bir yakınlaştırma türünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.PageWidth" olarak ayarlayın
// belgeyi sayfanın genişliğine sığdırmak için otomatik olarak yakınlaştırmak için.
// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.FullPage" olarak ayarlayın
// ilk sayfanın tamamını görünür kılmak için belgeyi otomatik olarak yakınlaştırmak için.
// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.TextFit" olarak ayarlayın
// ilk sayfanın iç metin kenar boşluklarına sığdırmak için belgeyi otomatik olarak yakınlaştırmak için.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Ayrıca bakınız

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)


