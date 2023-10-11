---
title: Fill.TextureAlignment
second_title: Aspose.Words für .NET-API-Referenz
description: Fill eigendom. Ruft die Ausrichtung für die Kacheltexturfüllung ab oder legt sie fest.
type: docs
weight: 190
url: /de/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Ruft die Ausrichtung für die Kacheltexturfüllung ab oder legt sie fest.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

### Beispiele

Zeigt, wie die Textur innerhalb der Form gefüllt und gekachelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Texturausrichtung auf die Formfüllung anwenden.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Verwenden Sie die Compliance-Option, um die Form mithilfe von DML zu definieren, wenn Sie „TextureAlignment“ erhalten möchten.
// Eigenschaft nach dem Speichern des Dokuments.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Siehe auch

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../fill/)
* Montage [Aspose.Words](../../../)


