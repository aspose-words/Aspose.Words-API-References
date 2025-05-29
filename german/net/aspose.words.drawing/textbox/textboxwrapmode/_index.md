---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextBox WrapMode-Eigenschaft, um den Textumbruch innerhalb von Formen zu verbessern und so die Klarheit und visuelle Attraktivität Ihres Designs zu steigern.
type: docs
weight: 110
url: /de/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Bestimmt, wie Text innerhalb einer Form umbrochen wird.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## Bemerkungen

Der Standardwert istSquare.

## Beispiele

Zeigt, wie ein Umbruchmodus für den Inhalt eines Textfelds festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Setzen Sie die Eigenschaft „TextBoxWrapMode“ auf „TextBoxWrapMode.None“, um die Breite des Textfelds zu erhöhen
// um Text unterzubringen, falls dieser groß genug ist.
// Setzen Sie die Eigenschaft "TextBoxWrapMode" auf "TextBoxWrapMode.Square" auf
// Den gesamten Text in das Textfeld einschließen und dabei seine Abmessungen beibehalten.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Siehe auch

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
