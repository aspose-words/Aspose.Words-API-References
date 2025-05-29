---
title: FieldIndex.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldIndex EntryType för att effektivt hantera indexposttyper för optimerad indexering och förbättrad sökprestanda.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

Hämtar eller anger en indexposttyp som används för att bygga indexet.

```csharp
public string EntryType { get; set; }
```

## Exempel

Visar hur man skapar ett INDEX-fält och sedan använder XE-fält för att fylla det med poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för text på vänster sida
// och sidan som innehåller XE-fältet till höger.
// Om XE-fälten har samma värde i sin "Text"-egenskap,
// INDEX-fältet grupperar dem i en post.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurera INDEX-fältet för att endast visa XE-fält som ligger inom gränserna
// av ett bokmärke med namnet "MainBookmark", och vars "EntryType"-egenskaper har värdet "A".
// För både INDEX- och XE-fälten använder egenskapen "EntryType" endast det första tecknet i sitt strängvärde.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// På en ny sida, börja bokmärket med ett namn som matchar värdet
// av INDEX-fältets egenskap "BookmarkName".
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX-fältet kommer att hämta den här posten eftersom den finns inuti bokmärket,
// och dess posttyp matchar även INDEX-fältets posttyp.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Infoga ett XE-fält som inte kommer att visas i INDEX eftersom posttyperna inte matchar.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Avsluta bokmärket och infoga ett XE-fält efteråt.
// Det är av samma typ som INDEX-fältet, men kommer inte att visas
// eftersom det ligger utanför bokmärkets gränser.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

### Se även

* class [FieldIndex](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
