---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.WrapType Sıralama. Metnin bir şeklin veya resmin etrafına nasıl sarılacağını belirtir C#'da.
type: docs
weight: 1400
url: /tr/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Metnin bir şeklin veya resmin etrafına nasıl sarılacağını belirtir.

```csharp
public enum WrapType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `3` | Şeklin etrafına sarılmış metin yok. Şekil metnin arkasına veya önüne yerleştirilir. |
| Inline | `0` | Şekil, metinle aynı katmanda kalır ve karakter olarak değerlendirilir. |
| TopBottom | `1` | Metin şeklin üstünde durur ve şeklin altındaki satırda yeniden başlar. |
| Square | `2` | Metni şeklin kare sınırlayıcı kutusunun tüm kenarlarının etrafına sarar. |
| Tight | `4` | Sınırlayıcı kutunun etrafına sarmak yerine şeklin kenarlarının etrafına sıkıca sarar. |
| Through | `5` | Sıkı ile aynıdır ancak şeklin açık olan tüm bölümlerinin içine sarılır. |

## Örnekler

Sayfanın ortasına kayan bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Çakışan metnin arkasında görünecek kayan bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

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

* property [WrapType](../shapebase/wraptype/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
