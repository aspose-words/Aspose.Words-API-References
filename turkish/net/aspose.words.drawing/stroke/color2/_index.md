---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words for .NET
description: Stroke Color2 mülk. Kontur için ikinci rengi tanımlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Kontur için ikinci rengi tanımlar.

```csharp
public Color Color2 { get; set; }
```

## Notlar

Bir için varsayılan değer[`Shape`](../../shape/) is White.

## Örnekler

Şekil kontur özelliklerinin nasıl işleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Konturlar, iki tonlu görüntü verileriyle tanımlanan bir desen oluşturmak için kullanılan iki renge sahip olabilir.
// Tek renkli konturlar Color2 özelliğini kullanmaz.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Ayrıca bakınız

* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
