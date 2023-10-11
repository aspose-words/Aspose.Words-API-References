---
title: ShapeBase.BehindText
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin metnin altında mı yoksa üstünde mi olacağını belirtir.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Şeklin metnin altında mı yoksa üstünde mi olacağını belirtir.

```csharp
public bool BehindText { get; set; }
```

### Notlar

Yalnızca üst düzey şekiller için etkilidir.

Varsayılan değer:`YANLIŞ`.

### Örnekler

Sayfanın ortasına kayan bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Çakışan metnin arkasında görünecek kayan bir resim ekleyin ve onu sayfanın ortasına hizalayın.
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
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


