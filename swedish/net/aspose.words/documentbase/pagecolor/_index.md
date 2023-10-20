---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words för .NET
description: DocumentBase PageColor fast egendom. Hämtar eller ställer in sidfärgen på dokumentet. Den här egenskapen är en enklare version avBackgroundShape  i C#.
type: docs
weight: 60
url: /sv/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Hämtar eller ställer in sidfärgen på dokumentet. Den här egenskapen är en enklare version av[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Anmärkningar

Den här egenskapen ger ett enkelt sätt att ange en helsidig färg för dokumentet. Genom att ställa in den här egenskapen skapas och ställs in en lämplig[`BackgroundShape`](../backgroundshape/).

Om sidfärgen inte är inställd (t.ex. det inte finns någon bakgrundsform i dokumentet) returneras Empty.

## Exempel

Visar hur du ställer in bakgrundsfärgen för alla sidor i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### Se även

* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
