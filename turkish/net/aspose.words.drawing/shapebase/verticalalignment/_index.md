---
title: ShapeBase.VerticalAlignment
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin dikey olarak nasıl konumlandırılacağını belirtir.
type: docs
weight: 560
url: /tr/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

Şeklin dikey olarak nasıl konumlandırılacağını belirtir.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
```

### Notlar

Varsayılan değer:None.

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

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


