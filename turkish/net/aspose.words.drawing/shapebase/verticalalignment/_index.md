---
title: ShapeBase.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım hassasiyeti ve görsel çekicilik için şeklinizin dikey konumlandırmasını optimize etmek üzere ShapeBase VerticalAlignment özelliğini keşfedin.
type: docs
weight: 600
url: /tr/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

Şeklin dikey olarak nasıl konumlandırılacağını belirtir.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
```

## Notlar

Varsayılan değer:None.

Sadece en üst seviyedeki yüzen şekiller için etkilidir.

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

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
