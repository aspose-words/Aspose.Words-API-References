---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ParagraphFormat SnapToGrid förbättrar layoutprecisionen genom att justera dina stycken med dokumentets rutnät för ett elegant utseende.
type: docs
weight: 300
url: /sv/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Anger om det aktuella stycket ska använda dokumentets rutnät per sida-inställningar vid layout av innehållet i stycket.

```csharp
public bool SnapToGrid { get; set; }
```

## Exempel

Visar hur man anger en gräns för antalet rader som varje sida får ha.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivera pitching och använd den sedan för att ställa in antalet rader per sida i det här avsnittet.
// En tillräckligt stor teckenstorlek kommer att trycka ner några rader till nästa sida för att undvika överlappande tecken.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
