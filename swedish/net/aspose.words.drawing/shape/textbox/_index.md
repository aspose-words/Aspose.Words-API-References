---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words för .NET
description: Anpassa dina textruteegenskaper för form för att förbättra textvisningen och förbättra den visuella attraktionskraften i dina designer. Lås upp kreativ potential idag!
type: docs
weight: 230
url: /sv/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

Definierar attribut som anger hur text visas i en form.

```csharp
public TextBox TextBox { get; }
```

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

* class [TextBox](../../textbox/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
