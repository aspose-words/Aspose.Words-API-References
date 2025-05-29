---
title: FieldIndex.UseYomi
linktitle: UseYomi
articleTitle: UseYomi
second_title: Aspose.Words för .NET
description: Förbättra din indexering med FieldIndex UseYomi-egenskapen. Aktivera enkelt yomi-text för förbättrad söksynlighet och bättre användarupplevelse.
type: docs
weight: 170
url: /sv/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

Hämtar eller anger om användning av yomi-text för indexposter ska aktiveras.

```csharp
public bool UseYomi { get; set; }
```

## Exempel

Visar hur man sorterar INDEX-fältposter fonetiskt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för Text på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// INDEX-posten samlar in alla XE-fält med matchande värden i egenskapen "Text"
// till en post istället för att skapa en post för varje XE-fält.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX-tabellen sorterar automatiskt sina poster efter värdena för deras Text-egenskaper i alfabetisk ordning.
// Ställ in INDEX-tabellen för att sortera poster fonetiskt med Hiragana istället.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Infoga 4 XE-fält, som skulle visas som poster i INDEX-fältets innehållsförteckning.
// Egenskapen "Text" kan innehålla ett ords stavning i Kanji, vars uttal kan vara tvetydigt,
// medan "Yomi"-versionen av ordet stavas exakt som det uttalas med hiragana.
// Om vi ställer in vårt INDEX-fält att använda Yomi, kommer det att sortera dessa poster
// med värdet på deras Yomi-egenskaper, istället för deras Text-värden.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Se även

* class [FieldIndex](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
