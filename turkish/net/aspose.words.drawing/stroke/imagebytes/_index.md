---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words for .NET
description: Stroke ImageBytes mülk. Kontur görüntüsü veya desen dolgusu için görüntüyü tanımlar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Kontur görüntüsü veya desen dolgusu için görüntüyü tanımlar.

```csharp
public byte[] ImageBytes { get; }
```

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
