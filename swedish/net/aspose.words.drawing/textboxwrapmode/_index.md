---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.TextBoxWrapMode-enum för att styra textbrytning i former, vilket förbättrar dokumentlayouter och designflexibilitet.
type: docs
weight: 1750
url: /sv/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Anger hur text radbryts inuti en form.

```csharp
public enum TextBoxWrapMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Square | `0` | Text radbryts inuti en form. |
| None | `2` | Text radbryts inte inuti en form. |

## Exempel

Visar hur man ställer in ett radbrytningsläge för innehållet i en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.None" för att öka textrutans bredd
// för att rymma text, om den är tillräckligt stor.
// Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.Square" för att
// radbryter all text inuti textrutan och bevarar dess dimensioner.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
