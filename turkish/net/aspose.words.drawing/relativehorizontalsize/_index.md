---
title: Enum RelativeHorizontalSize
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.RelativeHorizontalSize Sıralama. Bir şeklin veya metin çerçevesinin yatay olarak hesaplanan genişliğine göre göreceli olarak belirtir.
type: docs
weight: 1200
url: /tr/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Bir şeklin veya metin çerçevesinin yatay olarak hesaplanan genişliğine göre göreceli olarak belirtir.

```csharp
public enum RelativeHorizontalSize
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Margin | `0` | Genişliğin, sol ve sağ kenar boşlukları arasındaki boşluğa göre hesaplandığını belirtir. |
| Page | `1` | Genişliğin sayfa genişliğine göre hesaplandığını belirtir. |
| LeftMargin | `2` | Genişliğin sol kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| RightMargin | `3` | Genişliğin sağ kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| InnerMargin | `4` | Genişliğin iç kenar boşluğu alanı boyutuna, tek sayfalar için sol kenar boşluğu alanı boyutuna ve çift sayfalar için sağ kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| OuterMargin | `5` | Genişliğin dış kenar boşluğu alanı boyutuna, tek sayfalar için sağ kenar boşluğu alanı boyutuna ve çift sayfalar için sol kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| Default | `1` | Varsayılan değer:Margin . |

### Örnekler

Göreli boyut ve konumun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Mutlak boyut ve konuma sahip basit bir şekil ekleme.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Satır içi şekiller otomatik olarak mutlak birimlere dönüştürüldüğünden WrapType'ı WrapType.None olarak ayarlayın.
shape.WrapType = WrapType.None;

// Göreceli yatay boyutun kontrol edilmesi ve ayarlanması.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Kenar boşluğuna yatay boyut bağlamayı ayarlama.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Genişliği Marj genişliğinin %50'sine ayarlıyoruz.
    shape.WidthRelative = 50;
}

// Göreceli dikey boyutun kontrol edilmesi ve ayarlanması.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Dikey boyut ciltlemesini Kenar Boşluğuna ayarlama.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Yüksekliği Marj yüksekliğinin %30'una ayarlıyoruz.
    shape.HeightRelative = 30;
}

// Göreceli dikey konumun kontrol edilmesi ve ayarlanması.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // TopMargin'e konum bağlamayı ayarlıyoruz.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // TopMargin pozisyonunun göreceli Top'unu %30'a ayarlama.
    shape.TopRelative = 30;
}

// Göreceli yatay konumun kontrol edilmesi ve ayarlanması.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // RightMargin'e konum bağlamayı ayarlama.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Konumun göreli değeri negatif olabilir.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Ayrıca bakınız

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


