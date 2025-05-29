---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: .NET için Aspose.Words
description: Kişiselleştirilmiş bir görüntüleme deneyimi için Microsoft Word görüntüleme ayarlarınızı özelleştirmek üzere Belge GörünümüSeçenekleri özelliğini keşfedin.
type: docs
weight: 490
url: /tr/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Belgenin Microsoft Word'de nasıl görüntüleneceğini kontrol etmek için seçenekler sağlar.

```csharp
public ViewOptions ViewOptions { get; }
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

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
