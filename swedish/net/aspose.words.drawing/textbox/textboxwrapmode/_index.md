---
title: TextBox.TextBoxWrapMode
second_title: Aspose.Words för .NET API Referens
description: TextBox fast egendom. Bestämmer hur text radbryts inuti en form.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Bestämmer hur text radbryts inuti en form.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

### Anmärkningar

Standardvärdet ärSquare.

### Exempel

Visar hur man ställer in ett radbrytningsläge för innehållet i en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.None" för att öka textrutans bredd
// för att rymma text, om den är tillräckligt stor.
// Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.Square" till
// linda all text inuti textrutan, bevara dess dimensioner.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Se även

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../textbox/)
* hopsättning [Aspose.Words](../../../)


