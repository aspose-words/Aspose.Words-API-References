---
title: Enum TextBoxWrapMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.TextBoxWrapMode opsomming. Gibt an wie Text innerhalb einer Form umbrochen wird.
type: docs
weight: 1340
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
| None | `2` | Text wird nicht in eine Form umbrochen. |

### Beispiele

Zeigt, wie ein Umbruchmodus für den Inhalt eines Textfelds festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Setzen Sie die Eigenschaft „TextBoxWrapMode“ auf „TextBoxWrapMode.None“, um die Breite des Textfelds zu erhöhen
// um Text unterzubringen, sollte dieser groß genug sein.
// Setzen Sie die Eigenschaft „TextBoxWrapMode“ auf „TextBoxWrapMode.Square“.
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


