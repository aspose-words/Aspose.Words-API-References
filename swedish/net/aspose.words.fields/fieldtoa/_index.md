---
title: Class FieldToa
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldToa klass. Implementerar TOAfältet.
type: docs
weight: 2370
url: /sv/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Implementerar TOA-fältet.

```csharp
public class FieldToa : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldToa](fieldtoa/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | Hämtar eller ställer in namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | Hämtar eller ställer in integralkategorin för poster som ingår i tabellen. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | Hämtar eller ställer in teckensekvensen som används för att separera en tabell över behörighetsposter och dess sidnummer. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | Hämtar eller ställer in teckensekvensen som används för att separera två sidnummer i en sidnummerlista. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | Hämtar eller ställer in teckensekvensen som används för att separera början och slutet av ett sidintervall. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | Hämtar eller ställer in om formateringen av inmatningstexten i dokumentet ska tas bort från posten i auktoritetstabellen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | Hämtar eller ställer in namnet på en sekvens vars nummer ingår i sidnumret. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | Hämtar eller ställer in teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | Hämtar eller ställer in om kategorirubriken för posterna ska inkluderas i en auktoritetstabell. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | Hämtar eller ställer in om fem eller flera olika sidreferenser till same auktoritet ska ersättas med "passim", som används för att indikera att ett ord eller avsnitt förekommer ofta i det citerade arbetet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Skapar en tabell över myndigheter (det vill säga en lista över referenserna i ett juridiskt dokument, såsom referenser till ärenden, stadgar och regler, tillsammans med numren på sidorna där referenserna förekommer) med hjälp av posterna specificerade av TA fields.

### Exempel

Visar hur man bygger och anpassar en tabell över myndigheter med hjälp av TOA- och TA-fält.

```csharp
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

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


