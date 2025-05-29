---
title: FieldIndex.PageNumberListSeparator
linktitle: PageNumberListSeparator
articleTitle: PageNumberListSeparator
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldIndex PageNumberListSeparator för att enkelt anpassa sidnummerformateringen. Förbättra läsbarheten i ditt dokument idag!
type: docs
weight: 110
url: /sv/net/aspose.words.fields/fieldindex/pagenumberlistseparator/
---
## FieldIndex.PageNumberListSeparator property

Hämtar eller anger teckensekvensen som används för att separera två sidnummer i en sidnummerlista.

```csharp
public string PageNumberListSeparator { get; set; }
```

## Exempel

Visar hur man redigerar sidnummeravgränsaren i ett INDEX-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för Text på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// INDEX-posten grupperar XE-fält med matchande värden i egenskapen "Text"
// till en post istället för att skapa en post för varje XE-fält.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Om vårt INDEX-fält har en post för en grupp XE-fält,
// den här posten visar numret på varje sida som innehåller ett XE-fält som tillhör den här gruppen.
// Vi kan ställa in anpassade avgränsare för att anpassa utseendet på dessa sidnummer.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// Efter att vi har infogat dessa XE-fält kommer INDEX-fältet att visa "Första posten, på sidan(or) 2 & 3 & 4".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### Se även

* class [FieldIndex](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
