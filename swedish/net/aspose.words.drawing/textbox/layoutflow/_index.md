---
title: TextBox.LayoutFlow
second_title: Aspose.Words för .NET API Referens
description: TextBox fast egendom. Bestämmer flödet av textlayouten i en form.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Bestämmer flödet av textlayouten i en form.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

### Anmärkningar

Standardvärdet ärHorizontal.

### Exempel

Visar hur man ställer in orienteringen för text inuti en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Flytta dokumentbyggaren till inuti TextBox och lägg till text.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Ställ in egenskapen "LayoutFlow" för att ställa in en orientering för textinnehållet i denna textruta.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Se även

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../textbox/)
* hopsättning [Aspose.Words](../../../)


