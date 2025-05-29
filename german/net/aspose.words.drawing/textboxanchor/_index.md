---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.TextBoxAnchor für die präzise vertikale Ausrichtung von Formtext. Verbessern Sie mühelos die Formatierung Ihres Dokuments!
type: docs
weight: 1740
url: /de/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Gibt die für die vertikale Ausrichtung des Formtexts verwendeten Werte an.

```csharp
public enum TextBoxAnchor
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Top | `0` | Der Text wird oben im Textfeld ausgerichtet. |
| Middle | `1` | Der Text wird in der Mitte des Textfelds ausgerichtet. |
| Bottom | `2` | Der Text wird am unteren Rand des Textfelds ausgerichtet. |
| TopCentered | `3` | Der Text wird oben zentriert im Textfeld ausgerichtet. |
| MiddleCentered | `4` | Der Text wird mittig im Textfeld ausgerichtet. |
| BottomCentered | `5` | Der Text wird unten zentriert im Textfeld ausgerichtet. |
| TopBaseline | `6` | Der Text wird an der oberen Grundlinie des Textfelds ausgerichtet. |
| BottomBaseline | `7` | Der Text wird an der unteren Grundlinie des Textfelds ausgerichtet. |
| TopCenteredBaseline | `8` | Der Text wird an der oberen zentrierten Grundlinie des Textfelds ausgerichtet. |
| BottomCenteredBaseline | `9` | Der Text wird an der unteren zentrierten Grundlinie des Textfelds ausgerichtet. |

## Beispiele

Zeigt, wie der Textinhalt eines Textfelds vertikal ausgerichtet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Top" auf
// Richten Sie den Text in diesem Textfeld an der Oberseite der Form aus.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Middle" auf
// Richten Sie den Text in diesem Textfeld an der Mitte der Form aus.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Bottom" auf
// Richten Sie den Text in diesem Textfeld am unteren Rand der Form aus.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Die vertikale Ausrichtung von Text in Textfeldern ist ab Microsoft Word 2007 verfügbar.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
