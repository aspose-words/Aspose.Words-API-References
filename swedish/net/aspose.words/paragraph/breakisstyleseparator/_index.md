---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen Styckebrytning IsStyleSeparator förbättrar dokumentformateringen genom att tillåta blandade styckeformat för större designflexibilitet.
type: docs
weight: 20
url: /sv/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

Sant om denna styckebrytning är en stilseparator. En stilseparator gör att ett stycke kan bestå av delar som har olika styckestilar.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## Exempel

Visar hur man skriver text på samma rad som en rubrik i innehållsförteckningen och får den att inte visas i innehållsförteckningen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Infoga ett stycke med en stil som innehållsförteckningen hämtar som en post.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Båda dessa strängar finns i samma stycke och kommer därför att visas i samma innehållsförteckning.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Om vi infogar en stilseparator kan vi skriva mer text i samma stycke
// och använd en annan stil utan att den visas i innehållsförteckningen.
// Om vi använder en rubrikstil efter avgränsaren kan vi rita flera innehållsförteckningsposter från en och samma dokumenttextrad.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
