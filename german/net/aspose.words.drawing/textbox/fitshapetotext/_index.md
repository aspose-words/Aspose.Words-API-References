---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die FitShapeToText-Eigenschaft in Microsoft Word Formen automatisch anpasst, damit sie perfekt zu Ihrem Text passen, und so die Dokumentpräsentation verbessert.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Bestimmt, ob Microsoft Word die Form an den Text anpasst.

```csharp
public bool FitShapeToText { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie Sie die Größe eines Textfelds so anpassen, dass sein Inhalt genau hineinpasst.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Wenden Sie diese Werte auf beide Elemente an, damit die übergeordnete Form passt
// eng um den Textinhalt herum, wobei die von uns festgelegten Abmessungen ignoriert werden.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Siehe auch

* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
