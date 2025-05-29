---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextBox-Eigenschaft InternalMarginTop – steuern Sie den oberen Rand Ihrer Form in Punkten für ein präzises Layout und verbesserte Designflexibilität.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Gibt den inneren oberen Rand einer Form in Punkten an.

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

// Fügen Sie ein weiteres Textfeld mit bestimmten Rändern ein.
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
