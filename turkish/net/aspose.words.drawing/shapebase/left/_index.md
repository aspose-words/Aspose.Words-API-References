---
title: ShapeBase.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words for .NET
description: ShapeBase Left mülk. Şeklin içeren bloğunun sol kenarının konumunu alır veya ayarlar C#'da.
type: docs
weight: 370
url: /tr/net/aspose.words.drawing/shapebase/left/
---
## ShapeBase.Left property

Şeklin içeren bloğunun sol kenarının konumunu alır veya ayarlar.

```csharp
public double Left { get; set; }
```

## Notlar

Üst düzey bir şekil için değer nokta cinsindendir ve şekil bağlantısına göredir.

Bir gruptaki şekiller için değer, üst grubun koordinat alanında ve birimlerindedir.

Varsayılan değer 0'dır.

Yalnızca kayan şekiller için etkilidir.

## Örnekler

Kayan bir görüntünün nasıl ekleneceğini ve konumunun ve boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// "Left" özelliğinin değerini işlemek için şeklin "RelativeHorizontalPosition" özelliğini yapılandırın
 // şeklin sayfanın sol tarafına nokta cinsinden yatay uzaklığı olarak.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Şeklin sayfanın sol tarafından yatay uzaklığını 100 olarak ayarlayın.
shape.Left = 100;

// Şekli sayfanın üst kısmının 80pt altına konumlandırmak için "RelativeVerticalPosition" özelliğini benzer şekilde kullanın.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Boyutu korumak için genişliği otomatik olarak ölçeklendirecek şekilde şeklin yüksekliğini ayarlayın.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Bottom" ve "Right" özellikleri görüntünün alt ve sağ kenarlarını içerir.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
