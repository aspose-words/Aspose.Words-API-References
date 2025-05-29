---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ShowParagraphMarks i LayoutOptions förbättrar textformateringen genom att växla mellan synligheten av styckemarkeringar. Förbättra tydligheten i ditt dokument idag!
type: docs
weight: 90
url: /sv/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Hämtar eller anger om stycketecken återges. Standard är`falsk` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Exempel

Visar hur man visar stycketecken i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Lägg till några stycken och aktivera sedan stycketecken för att visa slutet på stycken
// med en pilcrow-symbol (¶) när vi renderar dokumentet.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Se även

* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
