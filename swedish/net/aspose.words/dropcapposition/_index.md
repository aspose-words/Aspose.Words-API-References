---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words för .NET
description: Aspose.Words.DropCapPosition uppräkning. Anger positionen för en drop captext i C#.
type: docs
weight: 1410
url: /sv/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Anger positionen för en drop cap-text.

```csharp
public enum DropCapPosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Stycket har inte ett drop cap. |
| Normal | `1` | Locket är placerat innanför textmarginalen på ankarstycket. |
| Margin | `2` | Drop cap är placerad utanför textmarginalen på ankarstycket. |

## Exempel

Visar hur man skapar en drop cap.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett stycke med en stor bokstav som texten i andra och tredje stycket börjar med.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// För närvarande kommer det andra och tredje stycket att visas under det första.
// Vi kan konvertera det första stycket som ett drop cap för de andra styckena via dess "ParagraphFormat"-objekt.
// Ställ in egenskapen "DropCapPosition" till "DropCapPosition.Margin" för att placera drop cap
// utanför den vänstra sidmarginalen om vår text är från vänster till höger.
// Ställ in egenskapen "DropCapPosition" till "DropCapPosition.Normal" för att placera drop cap inom sidmarginalerna
// och linda resten av texten runt den.
// "DropCapPosition.None" är standardtillståndet för alla stycken.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
