---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: .NET için Aspose.Words
description: Tasarımlarınızdaki şekil katmanlarını kontrol etmek, metin görünürlüğünü ve düzen hassasiyetini zahmetsizce artırmak için ShapeBase BehindText özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Şeklin metnin altında mı yoksa üstünde mi olduğunu belirtir.

```csharp
public bool BehindText { get; set; }
```

## Notlar

Sadece en üst seviye şekiller için etkilidir.

Varsayılan değer:`YANLIŞ`.

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

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
