---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: .NET için Aspose.Words
description: Şekiller ve metin çerçeveleri için dikey konumlandırmayı etkili bir şekilde tanımlamak ve belge düzenlerini geliştirmek için Aspose.Words.Drawing.RelativeVerticalPosition enum'unu keşfedin.
type: docs
weight: 1600
url: /tr/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Bir şeklin veya metin çerçevesinin dikey konumunun neye göre olduğunu belirtir.

```csharp
public enum RelativeVerticalPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Margin | `0` | Dikey konumlandırmanın sayfa kenar boşluklarına göre olacağını belirtir. |
| Page | `1` | Nesne sayfanın üst kenarına göre konumlandırılmıştır. |
| Paragraph | `2` | Nesne, bağlantı noktasını içeren paragrafın en üstüne göre konumlandırılmıştır. |
| Line | `3` | Belgelenmemiş. |
| TopMargin | `4` | Dikey konumlandırmanın geçerli sayfanın üst kenar boşluğuna göre olacağını belirtir. |
| BottomMargin | `5` | Dikey konumlandırmanın geçerli sayfanın alt kenar boşluğuna göre olacağını belirtir. |
| InsideMargin | `6` | Dikey konumlandırmanın geçerli sayfanın iç kenar boşluğuna göre olacağını belirtir. |
| OutsideMargin | `7` | Dikey konumlandırmanın geçerli sayfanın dış kenar boşluğuna göre olacağını belirtir. |
| TableDefault | `0` | Varsayılan değerMargin. |
| TextFrameDefault | `2` | Varsayılan değerParagraph. |

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

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
