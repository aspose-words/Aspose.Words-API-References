---
title: Bottom
second_title: Aspose.Words for .NET API Referansı
description: Şeklin içeren bloğunun alt kenarının konumunu alır.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

Şeklin içeren bloğunun alt kenarının konumunu alır.

```csharp
public double Bottom { get; }
```

### Notlar

Üst düzey bir şekil için değer, nokta cinsindendir ve şekil bağlantısına göredir.

Bir gruptaki şekiller için değer, üst grubun koordinat uzayında ve birimlerindedir.

### Örnekler

Yüzen bir görüntünün nasıl ekleneceğini ve konumunu ve boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// "Left" özelliğinin değerini işlemek için şeklin "RelativeHorizontalPosition" özelliğini yapılandırın
 // şeklin sayfanın sol tarafından nokta cinsinden yatay mesafesi olarak.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Şeklin sayfanın sol tarafından yatay mesafesini 100 olarak ayarlayın.
shape.Left = 100;

// Şekli 80pt sayfanın üst kısmından aşağıya konumlandırmak için "RelativeVerticalPosition" özelliğini benzer şekilde kullanın.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Boyutları korumak için genişliği otomatik olarak ölçekleyecek şeklin yüksekliğini ayarlayın.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Bottom" ve "Right" özellikleri görüntünün alt ve sağ kenarlarını içerir.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../../shapebase)
* ad alanı [Aspose.Words.Drawing](../../shapebase)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->