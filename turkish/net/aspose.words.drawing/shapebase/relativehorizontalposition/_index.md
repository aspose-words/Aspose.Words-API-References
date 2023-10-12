---
title: ShapeBase.RelativeHorizontalPosition
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin yatay olarak nasıl konumlandırılacağına göre belirtir.
type: docs
weight: 420
url: /tr/net/aspose.words.drawing/shapebase/relativehorizontalposition/
---
## ShapeBase.RelativeHorizontalPosition property

Şeklin yatay olarak nasıl konumlandırılacağına göre belirtir.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; set; }
```

### Notlar

Varsayılan değer:Column.

Yalnızca üst düzey kayan şekiller için etkilidir.

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

* enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


