---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Schriftart für einfachen Zugriff auf die Schriftformatierung. Verbessern Sie Ihre Designs mit anpassbaren Textstilen und einzigartigen Typografieoptionen.
type: docs
weight: 190
url: /de/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Bietet Zugriff auf die Schriftformatierung dieses Objekts.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
