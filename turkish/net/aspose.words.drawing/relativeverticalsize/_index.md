---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: .NET için Aspose.Words
description: Şekiller ve metin çerçeveleri için dikey yükseklik hesaplamalarını tanımlayan ve belge düzeni hassasiyetini artıran Aspose.Words.Drawing.RelativeVerticalSize enum'unu keşfedin.
type: docs
weight: 1610
url: /tr/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Bir şeklin veya metin çerçevesinin yüksekliğinin dikey olarak neye göre hesaplanacağını belirtir.

```csharp
public enum RelativeVerticalSize
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Margin | `0` | Yüksekliğin üst ve alt kenar boşlukları arasındaki boşluğa göre hesaplandığını belirtir. |
| Page | `1` | Yüksekliğin sayfa yüksekliğine göre hesaplandığını belirtir. |
| TopMargin | `2` | Yüksekliğin üst kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| BottomMargin | `3` | Yüksekliğin alt kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| InnerMargin | `4` | Yüksekliğin iç kenar boşluğu alanı boyutuna, tek sayfalar için üst kenar boşluğu alanı boyutuna ve çift sayfalar için alt kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| OuterMargin | `5` | Yüksekliğin dış kenar boşluğu alanı boyutuna, tek sayfalar için alt kenar boşluğu alanı boyutuna ve çift sayfalar için üst kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| Default | `1` | Varsayılan değerMargin . |

## Örnekler

Göreceli boyut ve konumun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Mutlak boyut ve konuma sahip basit bir şekil ekleniyor.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Satır içi şekiller otomatik olarak mutlak birimlere dönüştürüldüğünden WrapType'ı WrapType.None olarak ayarlayın.
shape.WrapType = WrapType.None;

// Göreceli yatay boyutu kontrol edip ayarlıyoruz.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Yatay boyut bağlamasını Margin'e ayarlama.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Genişliği Margin genişliğinin %50'sine ayarlıyorum.
    shape.WidthRelative = 50;
}

// Göreceli dikey boyutu kontrol edip ayarlıyoruz.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Dikey boyut bağlamasını Margin'e ayarlama.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Yükseklik, Margin yüksekliğinin %30'una ayarlanıyor.
    shape.HeightRelative = 30;
}

// Göreceli dikey konumun kontrolü ve ayarlanması.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // TopMargin'e pozisyon bağlamayı ayarlıyoruz.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Göreceli Üst Marj pozisyonunun %30'una ayarlanıyor.
    shape.TopRelative = 30;
}

// Göreceli yatay konumun kontrolü ve ayarlanması.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // RightMargin'e konum bağlamayı ayarlama.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Pozisyona göre değer negatif olabilir.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Ayrıca bakınız

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
