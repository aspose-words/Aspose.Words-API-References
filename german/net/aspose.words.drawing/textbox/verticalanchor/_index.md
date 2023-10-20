---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words für .NET
description: TextBox VerticalAnchor eigendom. Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an in C#.
type: docs
weight: 120
url: /de/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Bemerkungen

Der Standardwert istTop.

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

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
