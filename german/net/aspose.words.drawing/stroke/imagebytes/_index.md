---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der ImageBytes-Eigenschaft beeindruckende Strichbilder und einzigartige Musterfüllungen für Ihre Designs erstellen. Optimieren Sie Ihre visuellen Effekte noch heute!
type: docs
weight: 160
url: /de/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Definiert das Bild für ein Strichbild oder eine Musterfüllung.

```csharp
public byte[] ImageBytes { get; }
```

## Beispiele

Zeigt, wie Formstrichfunktionen verarbeitet werden.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Striche können zwei Farben haben, die zum Erstellen eines durch zweifarbige Bilddaten definierten Musters verwendet werden.
// Striche mit einer einzelnen Farbe verwenden die Color2-Eigenschaft nicht.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Siehe auch

* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
