---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: .NET için Aspose.Words
description: Microsoft Word'de belge görünümünü özelleştirmek, düzenleme deneyiminizi ve üretkenliğinizi artırmak için Aspose.Words.Settings.ViewOptions sınıfını keşfedin.
type: docs
weight: 6780
url: /tr/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Microsoft Word'de bir belgenin nasıl gösterileceğini kontrol eden çeşitli seçenekler sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Word Belgelerinin Seçenekleri ve Görünümüyle Çalışma](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) belgeleme makalesi.

```csharp
public class ViewOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Baskı düzeni görünümünde arka plan şeklinin görüntüsünü kontrol eder. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Metnin üstü ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Belgenin form tasarım modunda olup olmadığını belirtir. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Microsoft Word'deki görünüm modunu kontrol eder. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Belgenizi görüntülemek istediğiniz yüzdeyi alır veya ayarlar. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Pencerenin boyutuna göre bir yakınlaştırma değeri alır veya ayarlar. |

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

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
