---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.TextBoxAnchor opsomming. Gibt Werte an die für die vertikale Ausrichtung von Formtext verwendet werden in C#.
type: docs
weight: 1330
url: /de/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Gibt Werte an, die für die vertikale Ausrichtung von Formtext verwendet werden.

```csharp
public enum TextBoxAnchor
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Top | `0` | Text wird am oberen Rand des Textfelds ausgerichtet. |
| Middle | `1` | Text wird in der Mitte des Textfelds ausgerichtet. |
| Bottom | `2` | Text wird am unteren Rand des Textfelds ausgerichtet. |
| TopCentered | `3` | Der Text wird oben in der Mitte des Textfelds ausgerichtet. |
| MiddleCentered | `4` | Der Text wird in der Mitte des Textfelds ausgerichtet. |
| BottomCentered | `5` | Der Text wird am unteren Rand des Textfelds zentriert ausgerichtet. |
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

// Setzen Sie die Eigenschaft „VerticalAnchor“ auf „TextBoxAnchor.Top“.
// Richten Sie den Text in diesem Textfeld an der Oberseite der Form aus.
// Setzen Sie die Eigenschaft „VerticalAnchor“ auf „TextBoxAnchor.Middle“.
// Richten Sie den Text in diesem Textfeld an der Mitte der Form aus.
// Setzen Sie die Eigenschaft „VerticalAnchor“ auf „TextBoxAnchor.Bottom“.
// Richten Sie den Text in diesem Textfeld am unteren Rand der Form aus.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Die vertikale Ausrichtung von Text innerhalb von Textfeldern ist ab Microsoft Word 2007 verfügbar.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
