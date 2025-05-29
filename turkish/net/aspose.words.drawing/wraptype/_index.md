---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: .NET için Aspose.Words
description: Aspose.Words.Drawing.WrapType enum'unun profesyonel belge biçimlendirme için şekillerin ve resimlerin etrafındaki metin kaydırmayı nasıl geliştirdiğini keşfedin.
type: docs
weight: 1810
url: /tr/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Metnin bir şekil veya resmin etrafına nasıl sarılacağını belirtir.

```csharp
public enum WrapType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `3` | Şeklin etrafına metin sarma yok. Şekil metnin arkasına veya önüne yerleştirilir. |
| Inline | `0` | Şekil, metinle aynı katmanda kalır ve bir karakter olarak ele alınır. |
| TopBottom | `1` | Metin şeklin en üstünde durur ve şeklin altındaki satırda yeniden başlar. |
| Square | `2` | Metni şeklin kare sınırlayıcı kutusunun tüm kenarlarına sarar. |
| Tight | `4` | Sınırlayıcı kutunun etrafına sarılmak yerine şeklin kenarlarına sıkıca sarılır. |
| Through | `5` | Sıkı ile aynıdır, ancak şeklin açık olan herhangi bir kısmını sarar. |

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

* property [WrapType](../shapebase/wraptype/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
