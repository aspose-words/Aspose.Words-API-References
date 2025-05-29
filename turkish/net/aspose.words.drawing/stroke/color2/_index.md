---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: .NET için Aspose.Words
description: Stroke Color2 özelliğini keşfedin; canlı, göz alıcı görseller için tasarımlarınızı özelleştirilebilir ikinci bir vuruş rengiyle geliştirin.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Bir vuruş için ikinci bir renk tanımlar.

```csharp
public Color Color2 { get; set; }
```

## Notlar

Bir için varsayılan değer[`Shape`](../../shape/) x000d_ miWhite .

## Örnekler

Şekil kontur özelliklerinin nasıl işleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Vuruşlar, iki tonlu görüntü verileri tarafından tanımlanan bir desen oluşturmak için kullanılan iki renge sahip olabilir.
// Tek renkli vuruşlar Color2 özelliğini kullanmaz.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Ayrıca bakınız

* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
