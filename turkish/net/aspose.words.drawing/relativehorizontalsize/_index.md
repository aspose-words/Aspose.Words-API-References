---
title: RelativeHorizontalSize Enum
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: .NET için Aspose.Words
description: Belgelerinizdeki şekil ve metin çerçeve genişlikleri üzerinde hassas kontrol için Aspose.Words.Drawing.RelativeHorizontalSize enum'unu keşfedin. Biçimlendirmenizi bugün geliştirin!
type: docs
weight: 1590
url: /tr/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Bir şeklin veya metin çerçevesinin genişliğinin yatay olarak neye göre hesaplanacağını belirtir.

```csharp
public enum RelativeHorizontalSize
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Margin | `0` | Genişliğin sol ve sağ kenar boşlukları arasındaki boşluğa göre hesaplandığını belirtir. |
| Page | `1` | Genişliğin sayfa genişliğine göre hesaplandığını belirtir. |
| LeftMargin | `2` | Genişliğin sol kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| RightMargin | `3` | Genişliğin sağ kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| InnerMargin | `4` | Genişliğin iç kenar boşluğu alanı boyutuna göre hesaplandığını belirtir, tek sayfalar için sol kenar boşluğu alanı boyutuna ve çift sayfalar için sağ kenar boşluğu alanı boyutuna göre. |
| OuterMargin | `5` | Genişliğin dış kenar boşluğu alanı boyutuna göre hesaplandığını belirtir, tek sayfalar için sağ kenar boşluğu alanı boyutuna ve çift sayfalar için sol kenar boşluğu alanı boyutuna göre. |
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

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
