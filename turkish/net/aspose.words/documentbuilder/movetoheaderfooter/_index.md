---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: .NET için Aspose.Words
description: DocumentBuilder MoveToHeaderFooter yöntemi ile başlıklar ve altbilgiler arasında zahmetsizce gezinin, belge düzenleme verimliliğinizi artırın.
type: docs
weight: 580
url: /tr/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

İmleci geçerli bölümdeki bir üstbilgi veya altbilginin başına taşır.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | Taşınacak üstbilgi veya altbilgiyi belirtir. |

## Notlar

İmleci bir üstbilgi veya altbilgiye taşıdıktan sonra, geri kalanını kullanabilirsiniz[`DocumentBuilder`](../) Başlık veya altbilginin içeriğini değiştirmek için yöntemleri.

İlk sayfa için farklı başlıklar ve altbilgiler oluşturmak istiyorsanız, need öğesini ayarlamanız gerekir[`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

Çift ve tek sayfalar için farklı üstbilgiler ve altbilgiler oluşturmak istiyorsanız, need değerini ayarlamanız gerekir[`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

Kullanmak[`MoveToSection`](../movetosection/) Başlıktan ana metne geçmek için.

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

DocumentBuilder kullanılarak bir belgede üstbilgi ve altbilgilerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk, çift ve tek sayfalar için farklı üstbilgi ve altbilgi istediğimizi belirtin.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Başlıkları oluşturun, ardından her başlık türünü görüntülemek için belgeye üç sayfa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Ayrıca bakınız

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
