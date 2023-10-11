---
title: Enum RelativeHorizontalPosition
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.RelativeHorizontalPosition Sıralama. Bir şeklin veya metin çerçevesinin yatay konumunun göreli olduğunu belirtir.
type: docs
weight: 1190
url: /tr/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Bir şeklin veya metin çerçevesinin yatay konumunun göreli olduğunu belirtir.

```csharp
public enum RelativeHorizontalPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Margin | `0` | Yatay konumlandırmanın sayfa kenar boşluklarına göre olacağını belirtir. |
| Page | `1` | Nesne sayfanın sol kenarına göre konumlandırılır. |
| Column | `2` | Nesne, sütunun sol tarafına göre konumlandırılır. |
| Character | `3` | Nesne paragrafın sol tarafına göre konumlandırılır. |
| LeftMargin | `4` | Yatay konumlandırmanın sayfanın sol kenar boşluğuna göre olacağını belirtir. |
| RightMargin | `5` | Yatay konumlandırmanın sayfanın sağ kenar boşluğuna göre olacağını belirtir. |
| InsideMargin | `6` | Yatay konumlandırmanın, geçerli sayfanın iç kenar boşluğuna göre olacağını belirtir (tek sayfalarda sol kenar boşluğu, çift sayfalarda sağ kenar). |
| OutsideMargin | `7` | Yatay konumlandırmanın, geçerli sayfanın dış kenar boşluğuna göre olacağını belirtir (tek sayfalarda sağ kenar boşluğu, çift sayfalarda sol kenar boşluğu). |
| Default | `2` | Varsayılan değer:Column . |

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

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


