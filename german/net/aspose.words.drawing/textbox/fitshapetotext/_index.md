---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words für .NET
description: TextBox FitShapeToText eigendom. Legt fest ob Microsoft Word die Form an den Text anpasst in C#.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Legt fest, ob Microsoft Word die Form an den Text anpasst.

```csharp
public bool FitShapeToText { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie man die Größe eines Textfelds so anpasst, dass es genau in den Inhalt passt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Diese Werte auf diese beiden Elemente anwenden, damit die übergeordnete Form passt
// eng um den Textinhalt legen und dabei die von uns festgelegten Abmessungen ignorieren.
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
