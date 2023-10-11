---
title: Document.ViewOptions
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Belgenin Microsoft Wordde nasıl görüntüleneceğini kontrol etmek için seçenekler sunar.
type: docs
weight: 470
url: /tr/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Belgenin Microsoft Word'de nasıl görüntüleneceğini kontrol etmek için seçenekler sunar.

```csharp
public ViewOptions ViewOptions { get; }
```

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

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


