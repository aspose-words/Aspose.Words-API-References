---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: .NET için Aspose.Words
description: ShapeBase CanHaveImage özelliğini keşfedin; şekil türünüzün görsel çekiciliği artırmak için görselleri destekleyip desteklemediğini nasıl belirleyeceğinizi öğrenin!
type: docs
weight: 100
url: /tr/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Geri Döndürür`doğru` eğer şekil türü şeklin bir görüntüye sahip olmasına izin veriyorsa.

```csharp
public bool CanHaveImage { get; }
```

## Notlar

Microsoft Word'ün resimler için özel bir şekil türü olmasına rağmen, Microsoft Word belgelerinde bir grup şekli hariç herhangi bir shape 'nin bir resme sahip olabileceği anlaşılıyor, bu nedenle bu özellik şunu döndürür:`doğru` tüm şekiller hariç[`GroupShape`](../../groupshape/).

## Örnekler

Bir resmin nasıl ekleneceğini ve döndürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Resimli bir şekil ekle.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Görüntüyü saat yönünde 45 derece döndür.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
