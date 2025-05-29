---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SmartParagraphBreakReplacement i FindReplaceOptions. Kontrollera styckebrytningar enkelt för sömlös textformatering.
type: docs
weight: 170
url: /sv/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Hämtar eller anger ett booleskt värde som anger att det är tillåtet att ersätta stycket break när det inte finns något nästa systerparagraf.

Standardvärdet är`falsk`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Anmärkningar

Det här alternativet gör det möjligt att ersätta styckebrytning när det inte finns något nästa syskonstycke som alla underordnade -noder kan flyttas till, genom att hitta vilket (inte nödvändigtvis syskonstycke) nästa stycke efter det stycke som ersätts.

## Exempel

Visar hur man tar bort ett stycke från en tabellcell med en kapslad tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa tabell med stycke och en inre tabell i första cellen.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// När följande alternativ är satt till 'true', kommer Aspose.Words att ta bort styckets text
// helt med sitt stycketecken. Annars kommer Aspose.Words att härma Word och ta bort
// endast styckets text och lämnar stycketecknet intakt (när en tabell följer texten).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
