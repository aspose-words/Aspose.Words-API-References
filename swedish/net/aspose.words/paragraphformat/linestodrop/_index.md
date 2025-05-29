---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ParagraphFormat LinesToDrop förbättrar höjden på anfangen i dina dokument. Optimera din textlayout för fantastiska bilder!
type: docs
weight: 210
url: /sv/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Hämtar eller anger antalet rader i stycketexten som används för att beräkna anfangens höjd.

```csharp
public int LinesToDrop { get; set; }
```

## Exempel

Visar hur man ställer in storleken på en anfang.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändra egenskapen "LinesToDrop" för att ange ett stycke som en anfang,
// vilket kommer att förvandla det till en stor bokstav som kommer att dekorera nästa stycke.
// Ge den här egenskapen värdet 4 för att ge anfangen en höjd på fyra textrader.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Återställ egenskapen "LinesToDrop" till 0 för att göra nästa stycke till ett vanligt stycke.
// Texten i det här stycket bryts runt anfangsraden.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
