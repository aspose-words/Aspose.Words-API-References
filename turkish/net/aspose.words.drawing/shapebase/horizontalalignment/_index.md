---
title: ShapeBase.HorizontalAlignment
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin yatay olarak nasıl konumlandırılacağını belirtir.
type: docs
weight: 210
url: /tr/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Şeklin yatay olarak nasıl konumlandırılacağını belirtir.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

### Notlar

Varsayılan değerNone.

Yalnızca üst düzey kayan şekiller için etkilidir.

### Örnekler

Bir sayfanın ortasına kayan bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üst üste binen metnin arkasında görünecek kayan bir resim ekleyin ve onu sayfanın ortasına hizalayın.
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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


