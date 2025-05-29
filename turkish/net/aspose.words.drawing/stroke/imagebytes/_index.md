---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: .NET için Aspose.Words
description: Tasarımlarınız için çarpıcı kontur görüntüleri ve benzersiz desen dolguları oluşturmak için ImageBytes özelliğini nasıl kullanacağınızı keşfedin. Görsellerinizi bugün geliştirin!
type: docs
weight: 160
url: /tr/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Bir kontur görüntüsü veya desen dolgusu için görüntüyü tanımlar.

```csharp
public byte[] ImageBytes { get; }
```

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
