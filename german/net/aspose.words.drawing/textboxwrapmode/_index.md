---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.TextBoxWrapMode, um den Textumbruch in Formen zu steuern und so das Dokumentlayout und die Designflexibilität zu verbessern.
type: docs
weight: 1750
url: /de/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Gibt an, wie Text innerhalb einer Form umbrochen wird.

```csharp
public enum TextBoxWrapMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Square | `0` | Text wird innerhalb einer Form umbrochen. |
| None | `2` | Text wird innerhalb einer Form nicht umbrochen. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
