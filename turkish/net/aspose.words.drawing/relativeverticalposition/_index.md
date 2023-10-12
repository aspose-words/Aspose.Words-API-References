---
title: Enum RelativeVerticalPosition
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.RelativeVerticalPosition Sıralama. Bir şeklin veya metin çerçevesinin dikey konumunun göreli olduğunu belirtir.
type: docs
weight: 1210
url: /tr/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Bir şeklin veya metin çerçevesinin dikey konumunun göreli olduğunu belirtir.

```csharp
public enum RelativeVerticalPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Margin | `0` | Dikey konumlandırmanın sayfa kenar boşluklarına göre olacağını belirtir. |
| Page | `1` | Nesne sayfanın üst kenarına göre konumlandırılır. |
| Paragraph | `2` | Nesne, bağlantının bulunduğu paragrafın üst kısmına göre konumlandırılır. |
| Line | `3` | Belgelenmemiş. |
| TopMargin | `4` | Dikey konumlandırmanın geçerli sayfanın üst kenar boşluğuna göre olacağını belirtir. |
| BottomMargin | `5` | Dikey konumlandırmanın geçerli sayfanın alt kenar boşluğuna göre olacağını belirtir. |
| InsideMargin | `6` | Dikey konumlandırmanın geçerli sayfanın iç kenar boşluğuna göre olacağını belirtir. |
| OutsideMargin | `7` | Dikey konumlandırmanın geçerli sayfanın dış kenar boşluğuna göre olacağını belirtir. |
| TableDefault | `0` | Varsayılan değer:Margin . |
| TextFrameDefault | `2` | Varsayılan değer:Paragraph . |

### Örnekler

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

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


