---
title: Enum TextureAlignment
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.TextureAlignment opsomming. Gibt die Ausrichtung für die Kachelung der Texturfüllung an.
type: docs
weight: 1370
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
| Top | `1` | Obere Texturausrichtung. |
| TopRight | `2` | Texturausrichtung oben rechts. |
| Left | `3` | Linke Texturausrichtung. |
| Center | `4` | Texturausrichtung in der Mitte. |
| Right | `5` | Rechte Texturausrichtung. |
| BottomLeft | `6` | Texturausrichtung unten links. |
| Bottom | `7` | Ausrichtung der unteren Textur. |
| BottomRight | `8` | Texturausrichtung unten rechts. |
| None | `9` | Keine Texturausrichtung. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


