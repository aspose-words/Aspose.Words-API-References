---
title: Class ViewOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.ViewOptions sınıf. Bir belgenin Microsoft Wordde nasıl gösterileceğini kontrol eden çeşitli seçenekler sağlar.
type: docs
weight: 5950
url: /tr/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Bir belgenin Microsoft Word'de nasıl gösterileceğini kontrol eden çeşitli seçenekler sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Word Belgelerinin Seçenekleri ve Görünümüyle Çalışma](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) dokümantasyon makalesi.

```csharp
public class ViewOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Yazdırma düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Belgenin form tasarımı modunda olup olmadığını belirtir. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Microsoft Word'deki görüntüleme modunu kontrol eder. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Belgenizi görüntülemek istediğiniz yüzdeyi (10 ile 500 arasında) alır veya ayarlar. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Pencerenin boyutuna göre bir yakınlaştırma değeri alır veya ayarlar. |

### Örnekler

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

Microsoft Word'ün eski sürümlerinin yükleme sırasında bir belgeye uygulayacağı özel yakınlaştırma türünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.PageWidth" olarak ayarlayın
// belgeyi sayfanın genişliğine sığacak şekilde otomatik olarak yakınlaştırmak için.
// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.FullPage" olarak ayarlayın
// İlk sayfanın tamamını görünür hale getirmek için belgeyi otomatik olarak yakınlaştırmak için.
// Microsoft Word'ü almak için "ZoomType" özelliğini "ZoomType.TextFit" olarak ayarlayın
// belgeyi ilk sayfanın iç metin kenar boşluklarına sığacak şekilde otomatik olarak yakınlaştırmak için.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Ayrıca bakınız

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)


