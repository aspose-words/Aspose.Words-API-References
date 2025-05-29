---
title: Fill.PresetTexture
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die PresetTexture-Eigenschaft mühelos festlegen und Ihre Designs mit atemberaubenden Fülloptionen verbessern. Entfesseln Sie noch heute Ihr kreatives Potenzial!
type: docs
weight: 170
url: /de/net/aspose.words.drawing/fill/presettexture/
---
## Fill.PresetTexture property

Erhält eine[`PresetTexture`](../../presettexture/) für die Füllung.

```csharp
public PresetTexture PresetTexture { get; }
```

## Beispiele

Zeigt, wie die Textur innerhalb der Form gefüllt und gekachelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Texturausrichtung auf die Formfüllung anwenden.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren, wenn Sie „TextureAlignment“ erhalten möchten.
// Eigenschaft, nachdem das Dokument gespeichert wurde.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Siehe auch

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
