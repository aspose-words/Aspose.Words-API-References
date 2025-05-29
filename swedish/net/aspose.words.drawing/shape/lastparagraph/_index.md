---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words för .NET
description: Använd egenskapen LastParagraph för att enkelt hämta det sista stycket i din form, vilket förbättrar dokumentets layout och läsbarhet.
type: docs
weight: 130
url: /sv/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Hämtar det sista stycket i formen.

```csharp
public Paragraph LastParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
