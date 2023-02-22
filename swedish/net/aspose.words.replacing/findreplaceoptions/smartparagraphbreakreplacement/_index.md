---
title: FindReplaceOptions.SmartParagraphBreakReplacement
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. Hämtar eller ställer in ett booleskt värde som anger att det är tillåtet att ersätta stycke break när det inte finns något nästa syskonstycke.
type: docs
weight: 140
url: /sv/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Hämtar eller ställer in ett booleskt värde som anger att det är tillåtet att ersätta stycke break när det inte finns något nästa syskonstycke.

Standardvärdet är`falsk`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

### Anmärkningar

Det här alternativet gör det möjligt att ersätta styckebrytning när det inte finns något nästa syskonstycke som alla child -noder kan flyttas till, genom att hitta valfritt (inte nödvändigtvis syskon) nästa stycke efter stycket som ersätts.

### Exempel

Visar hur man tar bort stycke från en tabellcell med en kapslad tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa tabell med stycke och inre tabell i första cellen.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// När följande alternativ är satt till "true", kommer Aspose.Words att ta bort stycketexten
// helt med sitt styckemärke. Annars kommer Aspose.Words att efterlikna Word och ta bort
// endast styckets text och lämnar styckemärket intakt (när en tabell följer texten).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)


