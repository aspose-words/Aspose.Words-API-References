---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: .NET için Aspose.Words
description: Belgelerinizdeki şekiller ve metin çerçeveleri için hassas yatay konumlandırma tanımlamak üzere Aspose.Words.Drawing.RelativeHorizontalPosition enum'unu keşfedin.
type: docs
weight: 1580
url: /tr/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Bir şeklin veya metin çerçevesinin yatay konumunun neye göre olduğunu belirtir.

```csharp
public enum RelativeHorizontalPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Margin | `0` | Yatay konumlandırmanın sayfa kenar boşluklarına göre olacağını belirtir. |
| Page | `1` | Nesne sayfanın sol kenarına göre konumlandırılmıştır. |
| Column | `2` | Nesne, sütunun sol tarafına göre konumlandırılmıştır. |
| Character | `3` | Nesne paragrafın sol tarafına göre konumlandırılmıştır. |
| LeftMargin | `4` | Yatay konumlandırmanın sayfanın sol kenar boşluğuna göre olacağını belirtir. |
| RightMargin | `5` | Yatay konumlandırmanın sayfanın sağ kenar boşluğuna göre olacağını belirtir. |
| InsideMargin | `6` | Yatay konumlandırmanın, geçerli sayfanın iç kenar boşluğuna (tek sayfalarda sol kenar boşluğu, çift sayfalarda sağ kenar boşluğu) göre olacağını belirtir. |
| OutsideMargin | `7` | Yatay konumlandırmanın, geçerli sayfanın dış kenar boşluğuna (tek sayfalarda sağ kenar boşluğu, çift sayfalarda sol kenar boşluğu) göre olacağını belirtir. |
| Default | `2` | Varsayılan değerColumn . |

## Örnekler

Sayfanın ortasına kayan bir resmin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üst üste gelen metnin arkasında görünecek yüzen bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

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

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
