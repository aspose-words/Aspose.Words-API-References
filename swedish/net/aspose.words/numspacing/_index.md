---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.NumSpacing enum för att anpassa numeriskt avstånd för förbättrad dokumentformatering. Förbättra din textpresentation idag!
type: docs
weight: 5030
url: /sv/net/aspose.words/numspacing/
---
## NumSpacing enumeration

Anger möjliga värden där sifferavstånd kan visas.

```csharp
public enum NumSpacing
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | `0` | Anger att siffror visas i teckensnittets standardformat. |
| Proportional | `1` | Anger att siffrornas former, utformade som proportionellt avstånd, visas om de stöds av teckensnittet. |
| Tabular | `2` | Anger att siffrornas former, utformade som tabellform, visas om de stöds av teckensnittet. |

## Exempel

Visar hur man ställer in avståndstypen för siffran.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Den här effekten stöds endast i nyare versioner av MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
