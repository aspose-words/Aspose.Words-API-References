---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen DocumentBase PageColor för att enkelt anpassa dokumentets sidfärg. Förenkla designen med den här användarvänliga funktionen!
type: docs
weight: 70
url: /sv/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Hämtar eller ställer in dokumentets sidfärg. Den här egenskapen är en enklare version av[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Anmärkningar

Den här egenskapen ger ett enkelt sätt att ange en helfärgad sidfärg för dokumentet. Genom att ställa in den här egenskapen skapas och ställs en lämplig färg in.[`BackgroundShape`](../backgroundshape/).

Om sidfärgen inte är inställd (t.ex. om det inte finns någon bakgrundsform i dokumentet) returneras Empty.

## Exempel

Visar hur man ställer in bakgrundsfärgen för alla sidor i ett dokument.

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
