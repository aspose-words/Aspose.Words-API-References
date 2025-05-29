---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: .NET için Aspose.Words
description: Sayfa genişliğini noktalar halinde kolayca ayarlamak ve belge düzeninizi en iyi sunum için geliştirmek amacıyla PageSetup PageWidth özelliğini keşfedin.
type: docs
weight: 340
url: /tr/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

Sayfanın genişliğini noktalar halinde döndürür veya ayarlar.

```csharp
public double PageWidth { get; set; }
```

## Örnekler

Bir resmin nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Resmi her sayfada görünecek şekilde başlığa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Resmi sayfanın ortasına yerleştirin.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Kayan bir resmin nasıl ekleneceğini, konumunun ve boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Şeklin "RelativeHorizontalPosition" özelliğini "Left" özelliğinin değerini işleyecek şekilde yapılandırın
 // şeklin sayfanın sol tarafından yatay uzaklığı, nokta cinsinden.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Şeklin sayfanın sol tarafından yatay uzaklığını 100 olarak ayarlayın.
shape.Left = 100;

// Şekli sayfanın üstünden 80pt aşağıya yerleştirmek için benzer şekilde "RelativeVerticalPosition" özelliğini kullanın.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Şeklin yüksekliğini ayarlayın, bu sayede boyutlar korunarak genişlik otomatik olarak ölçeklenir.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Alt" ve "Sağ" özellikleri, görüntünün alt ve sağ kenarlarını içerir.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
