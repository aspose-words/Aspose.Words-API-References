---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words für .NET
description: TextBox InternalMarginTop eigendom. Gibt den inneren oberen Rand in Punkten für eine Form an in C#.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Gibt den inneren oberen Rand in Punkten für eine Form an.

```csharp
public double InternalMarginTop { get; set; }
```

## Bemerkungen

Der Standardwert ist 1/20 Zoll.

## Beispiele

Zeigt, wie interne Ränder für ein Textfeld festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein weiteres Textfeld mit bestimmten Rändern einfügen.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### Siehe auch

* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
