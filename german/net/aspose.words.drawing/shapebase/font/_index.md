---
title: ShapeBase.Font
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Bietet Zugriff auf die Schriftartformatierung dieses Objekts.
type: docs
weight: 190
url: /de/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Bietet Zugriff auf die Schriftartformatierung dieses Objekts.

```csharp
public Font Font { get; }
```

### Beispiele

Zeigt, wie man ein Textfeld einfügt und die Schriftart seines Inhalts festlegt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Setzen Sie die „Hidden“-Eigenschaft des „Font“-Objekts der Form auf „true“, um das Textfeld vor den Augen zu verbergen
// und reduzieren Sie den Platz, den es normalerweise einnehmen würde.
// Setzen Sie die Eigenschaft „Hidden“ des „Font“-Objekts der Form auf „false“, um das Textfeld sichtbar zu lassen.
shape.Font.Hidden = hideShape;

// Wenn die Form sichtbar ist, ändern wir ihr Aussehen über das Schriftartobjekt.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Den Builder aus dem Textfeld zurück in das Hauptdokument verschieben.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Siehe auch

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


