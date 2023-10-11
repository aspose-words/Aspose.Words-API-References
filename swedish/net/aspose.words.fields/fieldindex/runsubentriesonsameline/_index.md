---
title: FieldIndex.RunSubentriesOnSameLine
second_title: Aspose.Words för .NET API Referens
description: FieldIndex fast egendom. Hämtar eller ställer in om underposter ska köras på samma rad som huvudposten.
type: docs
weight: 140
url: /sv/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Hämtar eller ställer in om underposter ska köras på samma rad som huvudposten.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

### Exempel

Visar hur man arbetar med underposter i ett INDEX-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post kommer att visa XE-fältets textegenskapsvärde på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// INDEX-posten samlar alla XE-fält med matchande värden i egenskapen "Text"
// i en post i motsats till att göra en post för varje XE-fält.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// XE-fält som har en Text-egenskap vars värde blir rubriken för INDEX-posten.
// Om detta värde innehåller två strängsegment delade med ett kolon (INDEX-posten kommer att behandla :) avgränsare,
// det första segmentet är rubrik, och det andra segmentet blir underrubrik.
// INDEX-fältet grupperar först posterna alfabetiskt, sedan om det finns flera XE-fält med samma
// rubriker, kommer INDEX-fältet att undergruppera dem ytterligare efter värdena för dessa rubriker.
// Det kan finnas flera undergrupperingar, beroende på hur många gånger
// Textegenskaperna för XE-fält segmenteras så här.
// Som standard kommer en grupp för INDEX-fält att skapa en ny rad för varje underrubrik inom denna grupp.
// Vi kan ställa in RunSubentriesOnSameLine-flaggan till true för att behålla rubriken,
// och varje underrubrik för gruppen på en rad istället, vilket kommer att göra INDEX-fältet mer kompakt.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Infoga två XE-fält, var och en på en ny sida, och med samma rubrik som heter "Rubrik 1",
// som INDEX-fältet kommer att använda för att gruppera dem.
// Om RunSubentriesOnSameLine är falskt kommer INDEX-tabellen att skapa tre rader:
// en rad för grupperingsrubriken "Rubrik 1", och ytterligare en rad för varje underrubrik.
// Om RunSubentriesOnSameLine är sant, kommer INDEX-tabellen att skapa en enrads
// post som omfattar rubriken och varje underrubrik.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### Se även

* class [FieldIndex](../)
* namnutrymme [Aspose.Words.Fields](../../fieldindex/)
* hopsättning [Aspose.Words](../../../)


