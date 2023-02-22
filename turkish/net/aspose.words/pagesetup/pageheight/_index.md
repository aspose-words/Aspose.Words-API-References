---
title: PageSetup.PageHeight
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Sayfanın yüksekliğini nokta olarak döndürür veya ayarlar.
type: docs
weight: 300
url: /tr/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Sayfanın yüksekliğini nokta olarak döndürür veya ayarlar.

```csharp
public double PageHeight { get; set; }
```

### Örnekler

Bir resmin nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Resmi her sayfada görünecek şekilde başlığa ekleyin.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Resmi sayfanın ortasına yerleştirin.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Resmi her sayfada görünecek şekilde başlığa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Resmi sayfanın ortasına yerleştirin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


