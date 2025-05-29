---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase ParentParagraph-Eigenschaft – greifen Sie effizient auf den unmittelbar übergeordneten Absatz zu, um die Inhaltsverwaltung zu optimieren und die Organisation zu verbessern.
type: docs
weight: 430
url: /de/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Gibt den unmittelbar übergeordneten Absatz zurück.

```csharp
public Paragraph ParentParagraph { get; }
```

## Bemerkungen

Für untergeordnete Formen einer Gruppenform und untergeordnete Formen eines Office Math-Objekts gibt immer`null`.

## Beispiele

Zeigt, wie Sie ein Textfeld einfügen und die Schriftart seines Inhalts festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Setzen Sie die Eigenschaft „Hidden“ des Objekts „Font“ der Form auf „true“, um das Textfeld auszublenden
// und reduzieren Sie den Platz, den es normalerweise einnehmen würde.
// Setzen Sie die Eigenschaft „Hidden“ des „Font“-Objekts der Form auf „false“, um das Textfeld sichtbar zu lassen.
shape.Font.Hidden = hideShape;

// Wenn die Form sichtbar ist, ändern wir ihr Erscheinungsbild über das Schriftobjekt.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Verschieben Sie den Builder aus dem Textfeld zurück in das Hauptdokument.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Siehe auch

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
