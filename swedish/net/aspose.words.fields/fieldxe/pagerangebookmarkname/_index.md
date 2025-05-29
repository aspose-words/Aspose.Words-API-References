---
title: FieldXE.PageRangeBookmarkName
linktitle: PageRangeBookmarkName
articleTitle: PageRangeBookmarkName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldXE PageRangeBookmarkName – hantera bokmärkesnamn effektivt för exakt sidintervallspårning i dina dokument.
type: docs
weight: 60
url: /sv/net/aspose.words.fields/fieldxe/pagerangebookmarkname/
---
## FieldXE.PageRangeBookmarkName property

Hämtar eller anger namnet på bokmärket som markerar ett sidintervall som infogas som postens sidnummer.

```csharp
public string PageRangeBookmarkName { get; set; }
```

## Exempel

Visar hur man anger ett bokmärkes omspända sidor som ett sidintervall för en INDEX-fältpost.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för Text på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// INDEX-posten samlar in alla XE-fält med matchande värden i egenskapen "Text"
// till en post istället för att skapa en post för varje XE-fält.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// För INDEX-poster som visar sidintervall kan vi ange en separatorsträng
// som kommer att visas mellan numret på den första sidan och numret på den sista.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Om ett XE-fält namnger ett bokmärke med hjälp av egenskapen PageRangeBookmarkName,
// dess INDEX-post visar sidintervallet som bokmärket omfattar
// istället för numret på den sida som innehåller XE-fältet.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// Infoga ett bokmärke som börjar på sidan 3 och slutar på sidan 5.
// INDEX-posten för XE-fältet som refererar till detta bokmärke kommer att visa detta sidintervall.
// I vår tabell kommer INDEX-posten att visa "Min post, på sidan(or) 3 till 5".
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### Se även

* class [FieldXE](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
