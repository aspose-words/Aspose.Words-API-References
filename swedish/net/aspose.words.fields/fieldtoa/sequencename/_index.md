---
title: FieldToa.SequenceName
second_title: Aspose.Words för .NET API Referens
description: FieldToa fast egendom. Hämtar eller ställer in namnet på en sekvens vars nummer ingår i sidnumret.
type: docs
weight: 80
url: /sv/net/aspose.words.fields/fieldtoa/sequencename/
---
## FieldToa.SequenceName property

Hämtar eller ställer in namnet på en sekvens vars nummer ingår i sidnumret.

```csharp
public string SequenceName { get; set; }
```

### Exempel

Visar hur man bygger och anpassar en tabell över myndigheter med hjälp av TOA- och TA-fält.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga ett TOA-fält, vilket skapar en post för varje TA-fält i dokumentet,
    // visar långa citat och sidnummer för varje post.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Ställ in postkategorin för vårt bord. Denna TOA kommer nu bara att inkludera TA-fält
    // som har ett matchande värde i deras EntryCategory-egenskap.
    fieldToa.EntryCategory = "1";

    // Dessutom är kategorin över myndigheter i index 1 "Färden",
    // som kommer att dyka upp som vår tabells titel om vi ställer in denna variabel till true.
    fieldToa.UseHeading = true;

    // Vi kan ytterligare filtrera TA-fält genom att namnge ett bokmärke som de måste vara inom TOA-gränserna.
    fieldToa.BookmarkName = "MyBookmark";

    // Som standard visas en prickad sida bred flik mellan TA-fältets hänvisning
    // och dess sidnummer. Vi kan ersätta den med vilken text som helst vi lägger på den här fastigheten.
    // Att infoga ett tabbtecken kommer att bevara den ursprungliga fliken.
    fieldToa.EntrySeparator = " \t p.";

    // Om vi har flera TA-poster som delar samma långa citat,
    // alla deras respektive sidnummer kommer att visas på en rad.
    // Vi kan använda den här egenskapen för att ange en sträng som ska separera deras sidnummer.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Vi kan ställa in detta till sant för att få vår tabell att visa ordet "passim"
    // om det finns fem eller fler sidnummer på en rad.
    fieldToa.UsePassim = true;

    // Ett TA-fält kan referera till ett antal sidor.
    // Vi kan ange en sträng här som ska visas mellan start- och slutsidnumren för sådana intervall.
    fieldToa.PageRangeSeparator = " to ";

    // Formatet från TA-fälten kommer att överföras till vår tabell.
    // Vi kan inaktivera detta genom att ställa in flaggan RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Detta TA-fält kommer inte att visas som en post i TOA eftersom det är utanför
    // bokmärkets gränser som TOA:s BookmarkName-egenskap anger.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Detta TA-fält är inuti bokmärket,
    // men inmatningskategorin matchar inte tabellens, så TA-fältet kommer inte att inkludera den.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Denna post kommer att visas i tabellen.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // En TOA-tabell visar inte korta citat,
    // men vi kan använda dem som en stenografi för att referera till skrymmande källnamn som flera TA-fält refererar till.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Vi kan formatera sidnumret så att det blir fet/kursivt med hjälp av följande egenskaper.
    // Vi kommer fortfarande att se dessa effekter om vi ställer in vår tabell på att ignorera formatering.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Vi kan konfigurera TA-fält för att få deras TOA-poster att referera till en rad sidor som ett bokmärke sträcker sig över.
    // Observera att denna post refererar till samma källa som den ovan för att dela en rad i vår tabell.
    // Den här raden kommer att ha sidnumret för posten ovan och sidintervallet för denna post,
    // med tabellens sidlista och sidnummerintervallsavgränsare mellan sidnummer.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Om vi har aktiverat "Passim"-funktionen i vår tabell, kommer det att anropas att ha 5 eller fler TA-poster med samma källa.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Se även

* class [FieldToa](../)
* namnutrymme [Aspose.Words.Fields](../../fieldtoa/)
* hopsättning [Aspose.Words](../../../)


