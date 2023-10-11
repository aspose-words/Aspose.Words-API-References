---
title: ShapeBase.CanHaveImage
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. İadelerdoğru şekil türü şeklin bir resme sahip olmasına izin veriyorsa.
type: docs
weight: 100
url: /tr/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

İadeler`doğru` şekil türü, şeklin bir resme sahip olmasına izin veriyorsa.

```csharp
public bool CanHaveImage { get; }
```

### Notlar

Microsoft Word'ün görüntüler için özel bir şekil türü olmasına rağmen, Microsoft Word belgelerinde grup şekli dışındaki herhangi bir şekil 'nin bir görüntüye sahip olabileceği görülmektedir, bu nedenle bu özellik şunu döndürür:`doğru` hariç tüm şekiller için[`GroupShape`](../../groupshape/).

### Örnekler

Bir görüntünün nasıl ekleneceğini ve döndürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Resimli bir şekil ekleyin.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Resmi saat yönünde 45 derece döndürün.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


