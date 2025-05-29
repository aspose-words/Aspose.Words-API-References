---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.DropCapPosition-enum för att förbättra din dokumentdesign genom att definiera unika positioner för anfangstext för ett effektfullt visuellt tilltal.
type: docs
weight: 1820
url: /sv/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Anger positionen för en anfangstext.

```csharp
public enum DropCapPosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Stycket saknar anfang. |
| Normal | `1` | Anfangen placeras innanför textmarginalen på ankarstycket. |
| Margin | `2` | Anfangen placeras utanför textmarginalen på ankarstycket. |

## Exempel

Visar hur man skapar en anfang.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett stycke med en stor bokstav som texten i andra och tredje styckena börjar med.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// För närvarande kommer det andra och tredje stycket att visas under det första.
// Vi kan konvertera det första stycket till en anfang för de andra styckena via dess "ParagraphFormat"-objekt.
// Sätt egenskapen "DropCapPosition" till "DropCapPosition.Margin" för att placera anfangen
// utanför vänster sidmarginal om vår text är från vänster till höger.
// Ställ in egenskapen "DropCapPosition" till "DropCapPosition.Normal" för att placera anfangen inom sidmarginalerna
// och för att linda resten av texten runt den.
// "DropCapPosition.None" är standardläget för alla stycken.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
