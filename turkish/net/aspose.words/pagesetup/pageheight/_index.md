---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: .NET için Aspose.Words
description: Belgenizin yüksekliğini noktalar halinde etkin bir şekilde yönetmek, düzeninizi ve sunumunuzu geliştirmek için PageSetup PageHeight özelliğini keşfedin.
type: docs
weight: 310
url: /tr/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Sayfanın yüksekliğini noktalar halinde döndürür veya ayarlar.

```csharp
public double PageHeight { get; set; }
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

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
