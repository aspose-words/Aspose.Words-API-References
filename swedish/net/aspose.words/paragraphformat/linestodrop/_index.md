---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words för .NET
description: ParagraphFormat LinesToDrop fast egendom. Hämtar eller ställer in antalet rader i stycketexten som används för att beräkna fallhöjden i C#.
type: docs
weight: 210
url: /sv/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Hämtar eller ställer in antalet rader i stycketexten som används för att beräkna fallhöjden.

```csharp
public int LinesToDrop { get; set; }
```

## Exempel

Visar hur man ställer in storleken på en drop cap.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändra "LinesToDrop"-egenskapen för att beteckna ett stycke som ett drop cap,
// som kommer att göra det till en stor versal som kommer att pryda nästa stycke.
// Ge den här egenskapen värdet 4 för att ge drop cap höjden av fyra textrader.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Återställ egenskapen "LinesToDrop" till 0 för att göra nästa stycke till ett vanligt stycke.
// Texten i det här stycket kommer att lindas runt locket.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
