---
title: ShapeBase.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: .NET için Aspose.Words
description: Tasarımınızda şekillerin yatay konumlandırılmasını en iyi duruma getirerek gelişmiş düzen kontrolü sağlamak için ShapeBase Yatay Hizalama özelliğini keşfedin.
type: docs
weight: 240
url: /tr/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Şeklin yatay olarak nasıl konumlandırılacağını belirtir.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
