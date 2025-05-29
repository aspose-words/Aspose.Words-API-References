---
title: ShapeBase.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: .NET için Aspose.Words
description: Tasarımlarınızda hassas düzen kontrolü sağlayarak şekillerin dikey hizalamasını geliştirmek için ShapeBase RelativeVerticalPosition özelliğini keşfedin.
type: docs
weight: 470
url: /tr/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

Şeklin dikey olarak nasıl konumlandırıldığını belirtir.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

## Notlar

Varsayılan değer:Paragraph.

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

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
