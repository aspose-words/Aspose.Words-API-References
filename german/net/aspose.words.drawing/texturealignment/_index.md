---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.TextureAlignment für eine präzise Ausrichtung der Texturfüllung. Verbessern Sie Ihre Dokumentdesigns mit nahtlosen Kacheloptionen!
type: docs
weight: 1780
url: /de/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Gibt die Ausrichtung für die Kachelung der Texturfüllung an.

```csharp
public enum TextureAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| TopLeft | `0` | Texturausrichtung oben links. |
| Top | `1` | Ausrichtung der oberen Textur. |
| TopRight | `2` | Texturausrichtung oben rechts. |
| Left | `3` | Linke Texturausrichtung. |
| Center | `4` | Texturausrichtung zentrieren. |
| Right | `5` | Richtige Texturausrichtung. |
| BottomLeft | `6` | Texturausrichtung unten links. |
| Bottom | `7` | Ausrichtung der unteren Textur. |
| BottomRight | `8` | Texturausrichtung unten rechts. |
| None | `9` | Keine Texturausrichtung. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
