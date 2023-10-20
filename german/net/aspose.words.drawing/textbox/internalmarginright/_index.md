---
title: TextBox.InternalMarginRight
linktitle: InternalMarginRight
articleTitle: InternalMarginRight
second_title: Aspose.Words für .NET
description: TextBox InternalMarginRight eigendom. Gibt den inneren rechten Rand in Punkten für eine Form an in C#.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

Gibt den inneren rechten Rand in Punkten für eine Form an.

```csharp
public double InternalMarginRight { get; set; }
```

## Bemerkungen

Der Standardwert ist 1/10 Zoll.

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
