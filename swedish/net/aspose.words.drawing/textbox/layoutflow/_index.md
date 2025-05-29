---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen TextBox LayoutFlow förbättrar textlayouten i former, vilket förbättrar designflexibiliteten och läsbarheten för dina projekt.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Bestämmer flödet för textlayouten i en form.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## Anmärkningar

Standardvärdet ärHorizontal.

## Exempel

Visar hur man ställer in textens orientering inuti en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Flytta dokumentbyggaren till textrutan och lägg till text.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Ställ in egenskapen "LayoutFlow" för att ange en orientering för textinnehållet i den här textrutan.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Se även

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
