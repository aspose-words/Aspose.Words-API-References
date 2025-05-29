---
title: ShapeBase.Right
linktitle: Right
articleTitle: Right
second_title: .NET için Aspose.Words
description: Şeklinizin içeren bloğunun sağ kenar konumuna kolayca erişip hassas düzen kontrolü sağlamak için ShapeBase Right özelliğini keşfedin.
type: docs
weight: 490
url: /tr/net/aspose.words.drawing/shapebase/right/
---
## ShapeBase.Right property

Şeklin içeren bloğunun sağ kenarının konumunu alır.

```csharp
public double Right { get; }
```

## Notlar

En üst düzey bir şekil için değer, nokta cinsindendir ve şekil çapa noktasına göredir.

Bir gruptaki şekiller için değer, üst grubun koordinat alanında ve birimlerindedir.

## Örnekler

Kayan bir resmin nasıl ekleneceğini, konumunun ve boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Şeklin "RelativeHorizontalPosition" özelliğini "Left" özelliğinin değerini işleyecek şekilde yapılandırın
 // şeklin sayfanın sol tarafından yatay uzaklığı, nokta cinsinden.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Şeklin sayfanın sol tarafından yatay uzaklığını 100 olarak ayarlayın.
shape.Left = 100;

// Şekli sayfanın üstünden 80pt aşağıya yerleştirmek için benzer şekilde "RelativeVerticalPosition" özelliğini kullanın.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Şeklin yüksekliğini ayarlayın, bu sayede boyutlar korunarak genişlik otomatik olarak ölçeklenir.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Alt" ve "Sağ" özellikleri, görüntünün alt ve sağ kenarlarını içerir.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
