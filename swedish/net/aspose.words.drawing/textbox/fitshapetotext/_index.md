---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FitShapeToText i Microsoft Word automatiskt justerar former så att de passar perfekt i din text, vilket förbättrar dokumentpresentationen.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Avgör om Microsoft Word ska utöka formen så att den passar text.

```csharp
public bool FitShapeToText { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`.

## Exempel

Visar hur man får en textruta att ändra storlek så att den får plats med innehållet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Tillämpa dessa värden på båda dessa medlemmar för att få den överordnade formen att passa
// tätt runt textinnehållet, utan att tänka på de dimensioner vi har angett.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Se även

* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
