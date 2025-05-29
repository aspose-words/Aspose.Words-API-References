---
title: ShapeBase.RelativeVerticalSize
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım esnekliği ve hassasiyeti için şekillerin dikey boyutlarını kolayca ayarlamak üzere ShapeBase RelativeVerticalSize özelliğini keşfedin.
type: docs
weight: 480
url: /tr/net/aspose.words.drawing/shapebase/relativeverticalsize/
---
## ShapeBase.RelativeVerticalSize property

Şeklin dikey yöndeki göreli boyutunun değerini alır veya ayarlar.

```csharp
public RelativeVerticalSize RelativeVerticalSize { get; set; }
```

## Notlar

Varsayılan değer:Margin.

Yalnızca şu durumlarda etkilidir:[`HeightRelative`](../heightrelative/) ayarlandı.

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

* enum [RelativeVerticalSize](../../relativeverticalsize/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
