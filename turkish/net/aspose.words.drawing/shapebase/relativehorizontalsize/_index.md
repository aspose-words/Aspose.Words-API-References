---
title: ShapeBase.RelativeHorizontalSize
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words for .NET
description: ShapeBase RelativeHorizontalSize mülk. Şeklin göreceli boyutunun değerini yatay yönde alır veya ayarlar C#'da.
type: docs
weight: 430
url: /tr/net/aspose.words.drawing/shapebase/relativehorizontalsize/
---
## ShapeBase.RelativeHorizontalSize property

Şeklin göreceli boyutunun değerini yatay yönde alır veya ayarlar.

```csharp
public RelativeHorizontalSize RelativeHorizontalSize { get; set; }
```

## Notlar

Varsayılan değer:[`RelativeHorizontalSize`](../../relativehorizontalsize/).

Yalnızca şu durumlarda etkilidir:[`WidthRelative`](../widthrelative/) ayarlandı.

## Örnekler

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

* enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
