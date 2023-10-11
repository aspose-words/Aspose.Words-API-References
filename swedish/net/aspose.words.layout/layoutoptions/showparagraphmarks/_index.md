---
title: LayoutOptions.ShowParagraphMarks
second_title: Aspose.Words för .NET API Referens
description: LayoutOptions fast egendom. Hämtar eller ställer in en indikation på om stycketecken återges. Standard ärfalsk .
type: docs
weight: 90
url: /sv/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Hämtar eller ställer in en indikation på om stycketecken återges. Standard är`falsk` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

### Exempel

Visar hur man visar styckemärken i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Lägg till några stycken och aktivera sedan styckemärken för att visa slutet på stycken
// med en pilkråka (¶) symbol när vi renderar dokumentet.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Se även

* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../layoutoptions/)
* hopsättning [Aspose.Words](../../../)


