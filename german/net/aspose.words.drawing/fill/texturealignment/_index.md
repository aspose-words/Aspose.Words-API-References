---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words für .NET
description: Legen Sie die Eigenschaft „TextureAlignment“ fest, um die Kacheltexturfüllung zu optimieren. Passen Sie die Ausrichtung einfach an, um die Optik und Designpräzision zu verbessern.
type: docs
weight: 190
url: /de/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Ruft die Ausrichtung für die Kacheltexturfüllung ab oder legt sie fest.

```csharp
public TextureAlignment TextureAlignment { get; set; }
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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
